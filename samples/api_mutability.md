
---

<div align="center">
  <h1>API MUTABILITY</h1>
  <p>
    <a href="#setup"><kbd>Setup</kbd></a> &nbsp;•&nbsp; 
    <a href="#usage"><kbd>Usage</kbd></a>
  </p>
</div>

---

<a id="setup"></a>

<div align="center">
  <h2>❮ <code><b>Setup</b></code> ❯</h2> 
</div>

<code>This allows to "pseudo" change properties of the "globalThis.api" object, and use mutated methods/fields.</code><br>

```js
// run once in one place (code block)
{
  globalThis.__api__ = globalThis.api; // original object
  const sentinel_api = Object.create(null);
  const mutable_api = Object.assign({}, globalThis.api);

  Object.defineProperty(globalThis, "api", {
    get: () => sentinel_api,
    enumerable: true,
    configurable: true,
  });

  for (const key in mutable_api) {
    if (key === "thisPos" || key === "playerId" || key === "myId") {
      Object.defineProperty(sentinel_api, key, {
        get: () => {
          return globalThis[key];
        },
        set: (value) => {
          globalThis[key] = value;
        },
        enumerable: true,
        configurable: true,
      });
    } else {
      Object.defineProperty(sentinel_api, key, {
        get: () => {
          return mutable_api[key];
        },
        set: (value) => {
          mutable_api[key] = value;
        },
        enumerable: true,
        configurable: true,
      });
    }
  }

  void 0;
}
```

---

<a id="usage"></a>

<div align="center">
  <h2>❮ <code><b>Usage</b></code> ❯</h2> 
</div>

```js
// Returns a timestamp rounded down to the nearest multiple of 50
api.now = () => {
  let time = __api__.now();
  return time - (time % 50);
};
```

```js
api.now()
```

---
