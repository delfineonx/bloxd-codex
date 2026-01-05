---

<div align="center">
  <h1>POSES & STATES</h1>
  <p>
    <a href="#api-methods"><kbd>API Methods</kbd></a>
    &nbsp;•&nbsp; <a href="#player-poses"><kbd>Player Poses</kbd></a>
    &nbsp;•&nbsp; <a href="#physics-states"><kbd>Physics States</kbd></a>
  </p>
</div>

---

<a id="api-methods"></a>

<div align="center">
	<h2>❮ <code><b>API Methods</b></code> ❯</h2> 
</div>

```js
/**
 * Set the pose of the player.
 *
 * @param {PlayerId} playerId
 * @param {PlayerPose} pose
 * @param {[number, number, number]} [poseOffset]
 * @returns {void}
 */
setPlayerPose(playerId, pose, poseOffset)
```

```js
/**
 * Set physics state of player (vehicle type and tier) - partially works also on mobs.
 *
 * @param {PlayerId} playerId
 * @param {PlayerPhysicsStateData} physicsState
 * @returns {void}
 */
setPlayerPhysicsState(playerId, physicsState)
```

```js
/**
 * Get physics state for player.
 *
 * @param {PlayerId} playerId
 * @returns {PlayerPhysicsStateData}
 */
getPlayerPhysicsState(playerId)
```

---

<a id="player-poses"></a>

<div align="center">
	<h2>❮ <code><b>Player Poses</b></code> ❯</h2> 
</div>

```txt
standing
sitting
sleeping
gliding
driving
zombie
```

---

<a id="physics-states"></a>

<div align="center">
	<h2>❮ <code><b>Physics States</b></code> ❯</h2> 
</div>

---

