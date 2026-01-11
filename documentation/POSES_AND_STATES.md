
---

<div align="center">
  <h1>POSES & STATES</h1>
  <p>
    <a href="#api-methods"><kbd>API Methods</kbd></a> &nbsp;•&nbsp; 
    <a href="#player-poses"><kbd>Player Poses</kbd></a> &nbsp;•&nbsp; 
    <a href="#physics-states"><kbd>Physics States</kbd></a>
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

</details>

---

<a id="player-poses"></a>
<details open>
  <summary>
    <div align="center">
      <h2>❮ <code><b>Player Poses</b></code> ❯</h2>
    </div>
  </summary>

```js
"standing"
"sitting"
"gliding"
"driving"
"sleeping"
"riding"
"zombie"
```

</details>

---

<a id="physics-states"></a>
<details open>
  <summary>
    <div align="center">
      <h2>❮ <code><b>Physics States</b></code> ❯</h2>
    </div>
  </summary>

```ts
// tier meaning depends on type
type PlayerPhysicsStateData = { type: VehicleType; tier: VehicleTier };

enum VehicleType {
  PLAYER = 0,
  BOAT = 1,
  GLIDER = 2,
  BALLOON = 3,
  SLEEPING = 4,
  RIDING_MOB = 5,
}

type VehicleTier = PlayerTier | BoatTier | GliderTier | BalloonTier | SleepingTier | RidingMobTier;

enum PlayerTier {
  DEFAULT = 0,
}

enum BoatTier {
  NORMAL = 0,
  OBSIDIAN = 1,
}

enum GliderTier {
  WOOD = 0,
  IRON = 1,
  GOLD = 2,
  DIAMOND = 3,
}

enum BalloonTier {
  YELLOW = 0,
  WHITE = 1,
  RED = 2,
  PURPLE = 3,
  PINK = 4,
  ORANGE = 5,
  MAGENTA = 6,
  LIME = 7,
  LIGHT_GRAY = 8,
  LIGHT_BLUE = 9,
  GREEN = 10,
  GRAY = 11,
  CYAN = 12,
  BROWN = 13,
  BLUE = 14,
  BLACK = 15,
}

// aligns with the player's camera yaw direction (angleDir.theta)
enum SleepingTier {
  ROTATION_0 = 0, // 0
  ROTATION_1 = 1, // PI/2
  ROTATION_2 = 2, // PI
  ROTATION_3 = 3, // -PI/2
}

enum RidingMobTier {
  DEFAULT = 0,
}
```

</details>

---

