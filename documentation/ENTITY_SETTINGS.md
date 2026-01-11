
---

<div align="center">
  <h1>ENTITY SETTINGS</h1>
  <p>
    <a href="#api-methods"><kbd>API Methods</kbd></a> &nbsp;•&nbsp; 
    <a href="#settings"><kbd>Settings</kbd></a> &nbsp;•&nbsp; 
    <a href="#reference"><kbd>Reference</kbd></a>
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
 * Set a player's other-entity setting for a specific entity.
 *
 * @param {PlayerId} relevantPlayerId - player
 * @param {EntityId} targetedEntityId - player / mob / mesh
 * @param {Setting} settingName
 * @param {OtherEntitySettings[Setting]} settingValue
 * @returns {void}
 */
setOtherEntitySetting(relevantPlayerId, targetedEntityId, settingName, settingValue)
```

```js
/**
 * Set many of a player's other-entity settings for a specific entity.
 *
 * @param {PlayerId} relevantPlayerId - player
 * @param {EntityId} targetedEntityId - player / mob / mesh
 * @param {Partial<OtherEntitySettings>} settingsObject
 * @returns {void}
 */
setOtherEntitySettings(relevantPlayerId, targetedEntityId, settingsObject)
```

```js
/**
 * Get the value of a player's other-entity setting for a specific entity.
 *
 * @param {PlayerId} relevantPlayerId - player
 * @param {EntityId} targetedEntityId - player / mob / mesh
 * @param {Setting} settingName
 * @returns {OtherEntitySettings[Setting]}
 */
getOtherEntitySetting(relevantPlayerId, targetedEntityId, settingName)
```

```js
/**
 * Set every player's other-entity setting to a specific value for a particular entity.
 * "includeNewJoiners = true" means that new players joining the game will also have this other entity setting applied.
 *
 * @param {EntityId} targetedEntityId - player / mob / mesh
 * @param {Setting} settingName
 * @param {OtherEntitySettings[Setting]} settingValue
 * @param {boolean} [includeNewJoiners]
 * @returns {void}
 */
setTargetedPlayerSettingForEveryone(targetedEntityId, settingName, settingValue, includeNewJoiners)
```

```js
/**
 * Set a player's other-entity setting for every lifeform in the game.
 * "includeNewJoiners = true" means that new players joining the game will also have this other entity setting applied.
 *
 * @param {PlayerId} playerId
 * @param {Setting} settingName
 * @param {OtherEntitySettings[Setting]} settingValue
 * @param {boolean} [includeNewJoiners]
 * @returns {void}
 */
setEveryoneSettingForPlayer(playerId, settingName, settingValue, includeNewJoiners)
```

</details>

---

<a id="settings"></a>
<details open>
  <summary>
    <div align="center">
      <h2>❮ <code><b>Settings</b></code> ❯</h2>
    </div>
  </summary>

<div align="center">
  <table>
    <tr>
      <td valign="top" align="left"><h4>
        <a href="#opacity"><code>opacity</code></a><br>
        <a href="#zindex"><code>zIndex</code></a><br>
        <a href="#overlaycolour"><code>overlayColour</code></a><br>
        <a href="#canattack"><code>canAttack</code></a><br>
        <a href="#cansee"><code>canSee</code></a><br>
        <a href="#showdamageamounts"><code>showDamageAmounts</code></a><br>
        <a href="#killfeedcolour"><code>killfeedColour</code></a><br>
        <a href="#meshscaling"><code>meshScaling</code></a><br>
        <a href="#colorinlobbyleaderboard"><code>colorInLobbyLeaderboard</code></a><br>
        <a href="#lobbyleaderboardvalues"><code>lobbyLeaderboardValues</code></a><br>
        <a href="#nametaginfo"><code>nameTagInfo</code></a><br>
        <a href="#hasprioritynametag"><code>hasPriorityNametag</code></a><br>
        <a href="#namecolour"><code>nameColour</code></a><br>
      </h4></td>
    </tr>
  </table>
</div>

---

<a id="opacity"></a>

```js
/**
 * Opacity of the entity.
 * Fractional values will use dithering.
 * 0 opacity will hide the entity and its name tag.
 *
 * @type {number}
 */
opacity = 1
```

<a id="zindex"></a>

```js
/**
 * Rendering order of the entity; higher zIndex renders on top of lower ones.
 * 
 * @type {0 | 1}
 */
zIndex = 0
```

<a id="overlaycolour"></a>

```js
/**
 * Applies a colour tint to the entity when set, like the red tint when an entity gets hurt.
 * 
 * @type {string | null}
 */
overlayColour = null
```

<a id="canattack"></a>

```js
/**
 * Whether the entity can attack other entities, ignored if the targeted entity is invincible.
 * 
 * @type {boolean}
 */
canAttack = false
```

<a id="cansee"></a>

```js
/**
 * Whether the entity can be seen by the relevant player.
 * 
 * @type {boolean}
 */
canSee = true
```

<a id="showdamageamounts"></a>

```js
/**
 * Whether you can see damage amounts when shooting the entity.
 * 
 * @type {boolean}
 */
showDamageAmounts = true
```

<a id="killfeedcolour"></a>

```js
/**
 * The colour of kills in the killfeed. Defaults to blue for themselves and red for everyone else.
 * 
 * @type {string}
 */
killfeedColour = ""
```

<a id="meshscaling"></a>

```js
/**
 * Scaling of mesh nodes, see bottom of this page for `EntityMeshScalingMap`.
 * 
 * @type {EntityMeshScalingMap}
 */
meshScaling = {}
```

<a id="colorinlobbyleaderboard"></a>

```js
/**
 * The colour of the player in the lobby leaderboard.
 * 
 * @type {string}
 */
colorInLobbyLeaderboard = ""
```

<a id="lobbyleaderboardvalues"></a>

```js
/**
 * The values of the leaderboard.
 * 
 * @type {LobbyLeaderboardValues}
 */
lobbyLeaderboardValues = {}
```

<a id="nametaginfo"></a>

```js
/**
 * The name tag info of the player:
 * {
 *   backgroundColor?: string
 *   content?: StyledText[]
 *   subtitle?: StyledText[]
 *   subtitleBackgroundColor?: string
 * }
 * @type {NameTagInfo | null}
 */
nameTagInfo = null
```

<a id="hasprioritynametag"></a>

```js
/**
 * Whether the player has a priority name tag.
 * 
 * @type {boolean}
 */
hasPriorityNametag = false
```

<a id="namecolour"></a>

```js
/**
 * The colour of the player's name.
 * 
 * @type {string}
 */
nameColour = "default"
```

</details>

---

<a id="reference"></a>
<details open>
  <summary>
    <div align="center">
      <h2>❮ <code><b>Reference</b></code> ❯</h2>
    </div>
  </summary>

```ts
type StyledText = {
  str: string | EntityName | TranslatedText
  style?: {
    color?: string
    colour?: string
    fontWeight?: string
    fontSize?: string
    fontStyle?: string
    opacity?: number
  }
  clickableUrl?: string
}
```

```ts
type EntityName = {
  entityName: string
  style?: {
    color?: string
    colour?: string
  }
}
```

```ts
type TranslatedText = {
  translationKey: string
  params?: Record<string, string | number | boolean | EntityName>
}
```

</details>

---
