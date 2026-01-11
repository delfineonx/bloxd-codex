
---

<div align="center">
  <h1>SOUNDS</h1>
  <p>
    <a href="#api-methods"><kbd>API Methods</kbd></a> &nbsp;•&nbsp; 
	<a href="#resources"><kbd>Resources</kbd></a>
  </p>
</div>

---

<a id="api-methods"></a>
<details open>
  <summary>
    <div align="center">
      <h2>❮ <code><b>API Methods</b></code> ❯</h2>
    </div>
  </summary>

```js
/**
 * @param {PlayerId} playerId - hears the sound
 * @param {string} soundName - Can also be a prefix. If so, a random sound with that prefix will be played.
 * @param {number} volume - 0-1. If it's too quiet and volume is 1, normalise your sound in audacity.
 * @param {number} rate
 *   - The speed of playback.
 *   - Between 0.5 and 4.
 *   - Also affects pitch.
 *   - Lower playback = lower pitch.
 *   - Good for varying the sound (e.g. item pickup sound has a random rate between 1 and 1.5)
 * @param { {
 *   playerIdOrPos: PlayerId | [number, number, number]
 *   maxHearDist?: number
 *   refDistance?: number
 * } } [positionSettings]
 * @returns {void}
 */
playSound(playerId, soundName, volume, rate, positionSettings)
```

```js
/**
 * See documentation for `playSound()`.
 *
 * @param {string} soundName
 * @param {number} volume
 * @param {number} rate
 * @param { {
 *   playerIdOrPos: PlayerId | [number, number, number]
 *   maxHearDist?: number
 *   refDistance?: number
 * } } [positionSettings]
 * @param {PlayerId} [exceptPlayerId]
 * @returns {void}
 */
broadcastSound(soundName, volume, rate, positionSettings, exceptPlayerId)
```

```js
/**
 * See documentation for `playSound()`.
 *
 * @param {string} soundName
 * @param {number} volume
 * @param {number} rate
 * @param { {
 *   playerIdOrPos: PlayerId | [number, number, number]
 *   maxHearDist?: number
 *   refDistance?: number
 * } } [positionSettings]
 * @param {PlayerId} [predictedBy]
 * @returns {void}
 */
playClientPredictedSound(soundName, volume, rate, positionSettings, predictedBy)
```

</details>

---

<a id="resources"></a>
<details open>
  <summary>
    <div align="center">
      <h2>❮ <code><b>Resources</b></code> ❯</h2>
    </div>
  </summary>

<div align="center">
  <h4><code>Complete sounds list with audio by <i>FrostyCaveman</i></code><br></h4>
  <h4><a href="https://bloxdfc.pages.dev/sounds"><code>bloxdfc.pages.dev/sounds</code></a></h4>
</div>

> <h3><code><b>! NOTE</b></code></h3>
> You can get a random similar sound when you use common prefix (i.e. remove the numbers from the sound name of your choice).<br>

</details>

---

