
---

<div align="center">
  <h1>IU Tester</h1>
  <p>
    <a href="#intro"><kbd>Intro</kbd></a> &nbsp;•&nbsp; 
    <a href="#method"><kbd>Method</kbd></a> &nbsp;•&nbsp; 
    <a href="#setup"><kbd>Setup</kbd></a>
  </p>
</div>

<div align="center">
  <h4>
    ✦ <code><b>Credits</b></code> ✦<br>
    <b>Thanks to <code>Sulfrox</code> for creating and sharing these!</b>
  </h4> 
</div>

---

<a id="intro"></a>

<div align="center">
  <h2>❮ <code><b>Intro</b></code> ❯</h2> 
</div>

You can precisely measure how many *`interruption points/units (IU)`* a specific operation (or a group of operations) consumes by using *`3 code blocks setup`*. This approach is based on findings shared in the Discord thread  [**`Bloxd Interruption Notes`**](https://discord.com/channels/804347688946237472/1378177398679273522)  on coding-forum. 

---

<a id="method"></a>

<div align="center">
  <h2>❮ <code><b>Method</b></code> ❯</h2> 
</div>

<div align="left">
  <h3>〔 <code><b>Baseline run (A -> B -> C)</b></code> 〕</h3>
</div>

1. **Run `Code Block A`**  
   This resets the QuickJS interruption counter because the `while (true)` loop is guaranteed to trigger an interruption.

2. **Run `Code Block B` (without any inserted own code)**  
   `Code Block B` performs some fixed amount of "pre-computation" work, then enters an infinite loop that increments `interruption_counter`.

3. **Run `Code Block C`**  
   It logs to chat the measured `interruption_counter` value produced by `Code Block B`.

> [!IMPORTANT]
> Do not run any other code between A and B (including callbacks from `World Code`).  
> Any extra code executed between A and B will distort the result.

<div align="left">
  <h3>〔 <code><b>Measuring your own code</b></code> 〕</h3>
</div>

Repeat the same flow, but insert the code you want to test at the top of **`Code Block B`** (under the comment):

- Run **`A -> B (with your code) -> C`**
- Compare it to the baseline result

The difference between baseline and test result equals the IU cost of your inserted operation(s).

> [!TIP]
> When everything is done exactly as described, the highest reachable value is usually **`4985`**.  
> That makes repeated testing convenient:
>
> - Run once: `A -> B -> C` (initialize)
> - Then repeat: `D -> B -> C` (each new test)  
> - Compute: `IU = 4985 - result`
>
> (`Code Block D` cheaply forces an interruption again, so you don't need to rerun A every time)

---

<a id="setup"></a>

<div align="center">
  <h2>❮ <code><b>Setup</b></code> ❯</h2> 
</div>

<div align="left">
  <h3>〔 <code><b>Code Block A</b></code> 〕</h3>
</div>

```js
globalThis.array = [1];
for (let i = 0; i < 12; i++) {
  array = array.concat(array);
}
while (true) { }
```

<div align="left">
  <h3>〔 <code><b>Code Block B</b></code> 〕</h3>
</div>

```js
// code to test goes here

let pre_computation_count = 1000;
globalThis.interruption_counter = pre_computation_count * 3 + 1;

while (pre_computation_count--) {
  array.copyWithin(0, 1);
}

while (true) {
  interruption_counter++;
}
```

<div align="left">
  <h3>〔 <code><b>Code Block C</b></code> 〕</h3>
</div>

```js
interruption_counter
```

<div align="left">
  <h3>〔 <code><b>Code Block D</b></code> 〕</h3>
</div>

```js
while (true) { }
```

---
