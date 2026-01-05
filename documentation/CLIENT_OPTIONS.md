---

<div align="center">
  <h1>CLIENT OPTIONS</h1>
  <p>
    <a href="#api-methods"><kbd>API Methods</kbd></a>
    &nbsp;•&nbsp; <a href="#options"><kbd>Options</kbd></a>
    &nbsp;•&nbsp; <a href="#extra-info"><kbd>Extra Info</kbd></a>
  </p>
</div>

---

<a id="api-methods"></a>

<div align="center">
	<h2>❮ <code><b>API Methods</b></code> ❯</h2>
</div>


```js
/**
 * Modify a client option at runtime and send to the client if it changed.
 *
 * @param {PlayerId} playerId
 * @param {PassedOption} option - The name of the option
 * @param {ClientOptions[PassedOption]} value - The new value of the option
 * @returns {void}
 */
setClientOption(playerId, option, value)
```

```js
/**
 * Returns the current value of a client option.
 *
 * @param {PlayerId} playerId
 * @param {PassedOption} option
 * @returns {ClientOptions[PassedOption]}
 */
getClientOption(playerId, option)
```

```js
/**
 * Modify client options at runtime.
 *
 * @param {PlayerId} playerId
 * @param {Partial<ClientOptions>} optionsObject - An object which contains key value pairs of new settings. Example: { canChange: true, maxHealth: 200 }
 * @returns {void}
 */
setClientOptions(playerId, optionsObject)
```

```js
/**
 * Sets a client option to its default value.
 * This will be the value stored in your game's defaultClientOptions, otherwise Bloxd's default.
 *
 * @param {PlayerId} playerId
 * @param {ClientOption} option
 * @returns {void}
 */
setClientOptionToDefault(playerId, option)
```

---

<a id="options"></a>

<div align="center">
	<h2>❮ <code><b>Options</b></code> ❯</h2>
</div>

<div align="center">
  <table>
    <tbody>
      <tr>
        <td valign="top" align="left">
          <h4 align="center"><code>misc</code></h4>
          <div align="left">
            <a href="#crouchmobdetectionradiusmultiplier"><code>crouchMobDetectionRadiusMultiplier</code></a><br>
            <a href="#chatchannels"><code>chatChannels</code></a><br>
            <a href="#droppeditemscale"><code>droppedItemScale</code></a><br>
            <a href="#movementbasedfovscale"><code>movementBasedFovScale</code></a><br>
            <a href="#creative"><code>creative</code></a><br>
            <a href="#compasstarget"><code>compassTarget</code></a><br>
            <a href="#skybox"><code>skyBox</code></a><br>
            <a href="#defaultblock"><code>defaultBlock</code></a><br>
            <a href="#ttbmultiplier"><code>ttbMultiplier</code></a><br>
            <a href="#strictfluidbuckets"><code>strictFluidBuckets</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>can</code></h4>
          <div align="left">
            <a href="#canchange"><code>canChange</code></a><br>
            <a href="#cancraft"><code>canCraft</code></a><br>
            <a href="#canpickupitems"><code>canPickUpItems</code></a><br>
            <a href="#cancustomisechar"><code>canCustomiseChar</code></a><br>
            <a href="#canusezoomkey"><code>canUseZoomKey</code></a><br>
            <a href="#canaltaction"><code>canAltAction</code></a><br>
            <a href="#canseenametagsthroughwalls"><code>canSeeNametagsThroughWalls</code></a><br>
            <a href="#canpickblocks"><code>canPickBlocks</code></a><br>
            <a href="#canclimbwalls"><code>canClimbWalls</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>health &amp; shield</code></h4>
          <div align="left">
            <a href="#invincible"><code>invincible</code></a><br>
            <a href="#maxshield"><code>maxShield</code></a><br>
            <a href="#initialshield"><code>initialShield</code></a><br>
            <a href="#maxhealth"><code>maxHealth</code></a><br>
            <a href="#initialhealth"><code>initialHealth</code></a><br>
            <a href="#healthregenamount"><code>healthRegenAmount</code></a><br>
            <a href="#healthregeninterval"><code>healthRegenInterval</code></a><br>
            <a href="#healthregenstartafter"><code>healthRegenStartAfter</code></a><br>
          </div>
        </td>
      </tr>
      <tr>
        <td valign="top" align="left">
          <h4 align="center"><code>damage</code></h4>
          <div align="left">
            <a href="#dealingdamagemultiplier"><code>dealingDamageMultiplier</code></a><br>
            <a href="#dealingdamageheadmultiplier"><code>dealingDamageHeadMultiplier</code></a><br>
            <a href="#dealingdamagelegmultiplier"><code>dealingDamageLegMultiplier</code></a><br>
            <a href="#dealingdamagedefaultmultiplier"><code>dealingDamageDefaultMultiplier</code></a><br>
            <a href="#receivingdamagemultiplier"><code>receivingDamageMultiplier</code></a><br>
            <a href="#falldamage"><code>fallDamage</code></a><br>
            <a href="#stompdamagemultiplier"><code>stompDamageMultiplier</code></a><br>
            <a href="#stompdamageradius"><code>stompDamageRadius</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>effect</code></h4>
          <div align="left">
            <a href="#effectdamageduration"><code>effectDamageDuration</code></a><br>
            <a href="#effectspeedduration"><code>effectSpeedDuration</code></a><br>
            <a href="#effectdamagereductionduration"><code>effectDamageReductionDuration</code></a><br>
            <a href="#effecthealthregenduration"><code>effectHealthRegenDuration</code></a><br>
            <a href="#potioneffectduration"><code>potionEffectDuration</code></a><br>
            <a href="#splashpotioneffectduration"><code>splashPotionEffectDuration</code></a><br>
            <a href="#arrowpotioneffectduration"><code>arrowPotionEffectDuration</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>show</code></h4>
          <div align="left">
            <a href="#showplayersinunloadedchunks"><code>showPlayersInUnloadedChunks</code></a><br>
            <a href="#showkillfeed"><code>showKillfeed</code></a><br>
            <a href="#showbasicmovementcontrols"><code>showBasicMovementControls</code></a><br>
            <a href="#numclosestplayersvisible"><code>numClosestPlayersVisible</code></a><br>
            <a href="#showprogressbar"><code>showProgressBar</code></a><br>
          </div>
        </td>
      </tr>
      <tr>
        <td valign="top" align="left">
          <h4 align="center"><code>respawn</code></h4>
          <div align="left">
            <a href="#secstorespawn"><code>secsToRespawn</code></a><br>
            <a href="#useplayagainbutton"><code>usePlayAgainButton</code></a><br>
            <a href="#autorespawn"><code>autoRespawn</code></a><br>
            <a href="#respawnbuttontext"><code>respawnButtonText</code></a><br>
            <a href="#killstreakduration"><code>killstreakDuration</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>kart</code></h4>
          <div align="left">
            <a href="#karttargetspeedmult"><code>kartTargetSpeedMult</code></a><br>
            <a href="#kartspeedeffectmult"><code>kartSpeedEffectMult</code></a><br>
            <a href="#kartglidertargetheight"><code>kartGliderTargetHeight</code></a><br>
            <a href="#kartgroundheight"><code>kartGroundHeight</code></a><br>
            <a href="#kartapproachmaxspeedscalar"><code>kartApproachMaxSpeedScalar</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>text</code></h4>
          <div align="left">
            <a href="#middletextupper"><code>middleTextUpper</code></a><br>
            <a href="#middletextlower"><code>middleTextLower</code></a><br>
            <a href="#rightinfotext"><code>RightInfoText</code></a><br>
            <a href="#touchscreenactionbutton"><code>touchscreenActionButton</code></a><br>
            <a href="#crosshairtext"><code>crosshairText</code></a><br>
          </div>
        </td>
      </tr>
      <tr>
        <td valign="top" align="left">
          <h4 align="center"><code>friction</code></h4>
          <div align="left">
            <a href="#airfrictionscale"><code>airFrictionScale</code></a><br>
            <a href="#groundfrictionscale"><code>groundFrictionScale</code></a><br>
            <a href="#airaccscale"><code>airAccScale</code></a><br>
            <a href="#airmomentumconservation"><code>airMomentumConservation</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>camera</code></h4>
          <div align="left">
            <a href="#cameratint"><code>cameraTint</code></a><br>
            <a href="#playerzoom"><code>playerZoom</code></a><br>
            <a href="#zoomoutdistance"><code>zoomOutDistance</code></a><br>
            <a href="#maxplayerzoom"><code>maxPlayerZoom</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>speed</code></h4>
          <div align="left">
            <a href="#speedmultiplier"><code>speedMultiplier</code></a><br>
            <a href="#crouchingspeed"><code>crouchingSpeed</code></a><br>
            <a href="#flyspeedmultiplier"><code>flySpeedMultiplier</code></a><br>
          </div>
        </td>
      </tr>
      <tr>
        <td valign="top" align="left">
          <h4 align="center"><code>jump</code></h4>
          <div align="left">
            <a href="#jumpamount"><code>jumpAmount</code></a><br>
            <a href="#airjumpcount"><code>airJumpCount</code></a><br>
            <a href="#bounciness"><code>bounciness</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>can't</code></h4>
          <div align="left">
            <a href="#cantchangeerror"><code>cantChangeError</code></a><br>
            <a href="#cantbreakerror"><code>cantBreakError</code></a><br>
            <a href="#cantbuilderror"><code>cantBuildError</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>music</code></h4>
          <div align="left">
            <a href="#music"><code>music</code></a><br>
            <a href="#musicvolumelevel"><code>musicVolumeLevel</code></a><br>
          </div>
        </td>
      </tr>
      <tr>
        <td valign="top" align="left">
          <h4 align="center"><code>use</code></h4>
          <div align="left">
            <a href="#useinventory"><code>useInventory</code></a><br>
            <a href="#usefullinventory"><code>useFullInventory</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>fog</code></h4>
          <div align="left">
            <a href="#fogchunkdistanceoverride"><code>fogChunkDistanceOverride</code></a><br>
            <a href="#fogcolouroverride"><code>fogColourOverride</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>knockback</code></h4>
          <div align="left">
            <a href="#horizontalknockbackmultiplier"><code>horizontalKnockbackMultiplier</code></a><br>
            <a href="#verticalknockbackmultiplier"><code>verticalKnockbackMultiplier</code></a><br>
          </div>
        </td>
      </tr>
      <tr>
        <td valign="top" align="left">
          <h4 align="center"><code>aura</code></h4>
          <div align="left">
            <a href="#auraperlevel"><code>auraPerLevel</code></a><br>
            <a href="#maxauralevel"><code>maxAuraLevel</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>inventory</code></h4>
          <div align="left">
            <a href="#inventoryitemsmoveable"><code>inventoryItemsMoveable</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>leaderboard</code></h4>
          <div align="left">
            <a href="#lobbyleaderboardinfo"><code>lobbyLeaderboardInfo</code></a><br>
          </div>
        </td>
      </tr>
      <tr>
        <td valign="top" align="left">
          <h4 align="center"><code>bunnyhop</code></h4>
          <div align="left">
            <a href="#bunnyhopmaxmultiplier"><code>bunnyhopMaxMultiplier</code></a><br>
          </div>
        </td>
        <td valign="top" align="left"></td>
        <td valign="top" align="left"></td>
      </tr>
    </tbody>
  </table>
</div>


---

<div align="left">
    <h3>〔 <code><b>can</b></code> 〕</h3> 
</div>

<a id="canchange"></a>

```js
/**
 * Whether the player can change blocks
 * @type {boolean}
 */
canChange = true
```

<a id="cancraft"></a>

```js
/**
 * Whether to allow the player to craft items (useFullInventory must be true)
 * @type {boolean}
 */
canCraft = true
```

<a id="canpickupitems"></a>

```js
/**
 * Whether to allow the player to pick up items
 * @type {boolean}
 */
canPickUpItems = true
```

<a id="cancustomisechar"></a>

```js
/**
 * Whether the player can customise their character
 * @type {boolean}
 */
canCustomiseChar = true
```

<a id="canusezoomkey"></a>

```js
/**
 * Whether the player can use the zoom key
 * @type {boolean}
 */
canUseZoomKey = true
```

<a id="canaltaction"></a>

```js
/**
 * Whether the player can use the alt action key (right click on PC)
 * @type {boolean}
 */
canAltAction = true
```

<a id="canseenametagsthroughwalls"></a>

```js
/**
 * Whether the player can see name tags through walls
 * @type {boolean}
 */
canSeeNametagsThroughWalls = true
```

<a id="canpickblocks"></a>

```js
/**
 * Whether the player can pick blocks (middle mouse click on PC), ignored if creative is false
 * @type {boolean}
 */
canPickBlocks = true
```

<a id="canclimbwalls"></a>

```js
/**
 * Whether the player can climb walls
 * @type {boolean}
 */
canClimbWalls = false
```

---

<div align="left">
    <h3>〔 <code><b>can't</b></code> 〕</h3> 
</div>

<a id="cantchangeerror"></a>

```js
/**
 * Error message for when the player fails to change a block
 * @type {string | CustomTextStyling}
 */
cantChangeError = "You cannot modify this block"
```

<a id="cantbreakerror"></a>

```js
/**
 * Error message for when the player fails to break a block
 * @type {string | CustomTextStyling}
 */
cantBreakError = null
```

<a id="cantbuilderror"></a>

```js
/**
 * Error message for when the player fails to place a block
 * @type {string | CustomTextStyling}
 */
cantBuildError = null
```

---

<div align="left">
    <h3>〔 <code><b>use</b></code> 〕</h3> 
</div>

<a id="useinventory"></a>

```js
/**
 * Whether to allow the player to use the inventory (disabling also disables the hotbar)
 * @type {boolean}
 */
useInventory = true
```

<a id="usefullinventory"></a>

```js
/**
 * Enables the UI of the full inventory
 * @type {boolean}
 */
useFullInventory = true
```

---

<div align="left">
    <h3>〔 <code><b>show</b></code> 〕</h3> 
</div>

<a id="showplayersinunloadedchunks"></a>

```js
/**
 * Whether to show the player in unloaded chunks
 * @type {boolean}
 */
showPlayersInUnloadedChunks = false
```

<a id="showkillfeed"></a>

```js
/**
 * Whether to show the killfeed
 * @type {boolean}
 */
showKillfeed = true
```

<a id="showbasicmovementcontrols"></a>

```js
/**
 * Whether to show basic movement controls
 * @type {boolean}
 */
showBasicMovementControls = true
```

<a id="numclosestplayersvisible"></a>

```js
/**
 * If set, clients will only be able to see the closest x players
 * @type {number | null}
 */
numClosestPlayersVisible = null
```

<a id="showprogressbar"></a>

```js
/**
 * Whether to show the progress bar
 * @type {boolean}
 */
showProgressBar = false
```

---

<div align="left">
    <h3>〔 <code><b>speed</b></code> 〕</h3> 
</div>


<a id="speedmultiplier"></a>

```js
/**
 * Speed multiplier for the player
 * @type {number}
 */
speedMultiplier = 1
```

<a id="crouchingspeed"></a>

```js
/**
 * Speed multiplier for the player when crouching
 * @type {number}
 */
crouchingSpeed = 2
```

<a id="flyspeedmultiplier"></a>

```js
/**
 * Multiplier for the flying speed in creative mode
 * @type {number}
 */
flySpeedMultiplier = 1.5
```

---

<div align="left">
    <h3>〔 <code><b>jump</b></code> 〕</h3> 
</div>

<a id="jumpamount"></a>

```js
/**
 * Amount of jump power the player has
 * @type {number}
 */
jumpAmount = 8
```

<a id="airjumpcount"></a>

```js
/**
 * Amount of air jumps the player has
 * @type {number}
 */
airJumpCount = 0
```

<a id="bounciness"></a>

```js
/**
 * How much the player bounces off of solid blocks (1 = every block acts as a mushroom)
 * @type {number}
 */
bounciness = 0
```

---

<div align="left">
    <h3>〔 <code><b>bunnyhop</b></code> 〕</h3> 
</div>

<a id="bunnyhopmaxmultiplier"></a>

```js
/**
 * Maximum multiplier for jump height when bunnyhopping
 * @type {number}
 */
bunnyhopMaxMultiplier = 1.3
```

---

<div align="left">
    <h3>〔 <code><b>music</b></code> 〕</h3> 
</div>

<a id="music"></a>

```js
/**
 * The music track to play in the background
 * @type {Song | null}
 */
music = null
```

<a id="musicvolumelevel"></a>

```js
/**
 * Volume level for the music
 * @type {number}
 */
musicVolumeLevel = 0.6
```

---

<div align="left">
    <h3>〔 <code><b>camera</b></code> 〕</h3> 
</div>

<a id="cameratint"></a>

```js
/**
 * RGBA array [r, g, b, a] for camera tint; values 0..1
 * @type {[number, number, number, number] | null}
 */
cameraTint = null
```

<a id="playerzoom"></a>

```js
/**
 * Default camera zoom level for the player
 * @type {number}
 */
playerZoom = 0
```

<a id="zoomoutdistance"></a>

```js
/**
 * Distance to zoom the camera out to
 * @type {number}
 */
zoomOutDistance = 3
```

<a id="maxplayerzoom"></a>

```js
/**
 * Maximum camera zoom level for the player
 * @type {number}
 */
maxPlayerZoom = 15
```

---

<div align="left">
    <h3>〔 <code><b>fog</b></code> 〕</h3> 
</div>

<a id="fogchunkdistanceoverride"></a>

```js
/**
 * Fog distance which overrides graphic settings; uses settings if null
 * @type {number | null}
 */
fogChunkDistanceOverride = null
```

<a id="fogcolouroverride"></a>

```js
/**
 * RGB string for fog colour override (e.g. #ffffff)
 * @type {string | null}
 */
fogColourOverride = null
```

---

<div align="left">
    <h3>〔 <code><b>leaderboard</b></code> 〕</h3> 
</div>

<a id="lobbyleaderboardinfo"></a>

```js
/**
 * Columns of the lobby leaderboard
 * @type {LobbyLeaderboardInfo}
 */
lobbyLeaderboardInfo = { /* ... */ }
```

---

<div align="left">
    <h3>〔 <code><b>text</b></code> 〕</h3> 
</div>

<a id="middletextupper"></a>

```js
/**
 * Large text to display in the middle of the screen
 * @type {string | CustomTextStyling}
 */
middleTextUpper = ""
```

<a id="middletextlower"></a>

```js
/**
 * Small text to display in the middle of the screen
 * @type {string | CustomTextStyling}
 */
middleTextLower = ""
```

<a id="rightinfotext"></a>

```js
/**
 * Text to display in the right info box
 * @type {string | CustomTextStyling}
 */
RightInfoText = ""
```

<a id="touchscreenactionbutton"></a>

```js
/**
 * Contents of the action button; supports custom text styling
 * @type {string | CustomTextStyling | null}
 */
touchscreenActionButton = null
```

<a id="crosshairtext"></a>

```js
/**
 * Text to display at the crosshair; supports custom text styling
 * @type {string | CustomTextStyling}
 */
crosshairText = ""
```

---

<div align="left">
    <h3>〔 <code><b>inventory</b></code> 〕</h3> 
</div>

<a id="inventoryitemsmoveable"></a>

```js
/**
 * Whether the player can move items in their inventory (requires useInventory)
 * @type {boolean}
 */
inventoryItemsMoveable = true
```

---

<div align="left">
    <h3>〔 <code><b>health & shield</b></code> 〕</h3> 
</div>

<a id="invincible"></a>

```js
/**
 * Whether the player is invincible
 * @type {boolean}
 */
invincible = false
```

<a id="maxshield"></a>

```js
/**
 * Maximum shield the player can have
 * @type {number}
 */
maxShield = 100
```

<a id="initialshield"></a>

```js
/**
 * Shield upon joining or respawning
 * @type {number}
 */
initialShield = 0
```

<a id="maxhealth"></a>

```js
/**
 * Maximum health the player can have
 * @type {number}
 */
maxHealth = 100
```

<a id="initialhealth"></a>

```js
/**
 * Health upon joining or respawning (can be null to disable health)
 * @type {number | null}
 */
initialHealth = 100
```

<a id="healthregenamount"></a>

```js
/**
 * Fraction of max health that regens each regen tick
 * @type {number}
 */
healthRegenAmount = 0.05
```

<a id="healthregeninterval"></a>

```js
/**
 * How often health regen is ticked (ms)
 * @type {number}
 */
healthRegenInterval = 4000
```

<a id="healthregenstartafter"></a>

```js
/**
 * How long after damage to start regen again (ms)
 * @type {number}
 */
healthRegenStartAfter = 5000
```

---

<div align="left">
    <h3>〔 <code><b>effect</b></code> 〕</h3> 
</div>

<a id="effectdamageduration"></a>

```js
/**
 * Duration of the +damage effect from plum (ms)
 * @type {number}
 */
effectDamageDuration = 8000
```

<a id="effectspeedduration"></a>

```js
/**
 * Duration of +speed effect from cracked coconut (ms)
 * @type {number}
 */
effectSpeedDuration = 8000
```

<a id="effectdamagereductionduration"></a>

```js
/**
 * Duration of +damage reduction effect from pear (ms)
 * @type {number}
 */
effectDamageReductionDuration = 13000
```

<a id="effecthealthregenduration"></a>

```js
/**
 * Duration of +health regen effect from cherry (ms)
 * @type {number}
 */
effectHealthRegenDuration = 5000
```

<a id="potioneffectduration"></a>

```js
/**
 * Duration of potion effects (ms)
 * @type {number}
 */
potionEffectDuration = 12000
```

<a id="splashpotioneffectduration"></a>

```js
/**
 * Duration of splash potion effects (ms)
 * @type {number}
 */
splashPotionEffectDuration = 8000
```

<a id="arrowpotioneffectduration"></a>

```js
/**
 * Duration of arrow potion effects (ms)
 * @type {number}
 */
arrowPotionEffectDuration = 6000
```

---

<div align="left">
    <h3>〔 <code><b>respawn</b></code> 〕</h3> 
</div>

<a id="secstorespawn"></a>

```js
/**
 * After dying, the player can respawn after this many seconds
 * @type {number}
 */
secsToRespawn = 3
```

<a id="useplayagainbutton"></a>

```js
/**
 * When dead, show a play again button (mostly for session-based games)
 * @type {boolean}
 */
usePlayAgainButton = false
```

<a id="autorespawn"></a>

```js
/**
 * If true, player respawns automatically after secsToRespawn seconds
 * @type {boolean}
 */
autoRespawn = false
```

<a id="respawnbuttontext"></a>

```js
/**
 * Text to show on respawn button
 * @type {string}
 */
respawnButtonText = "general:respawn"
```

<a id="killstreakduration"></a>

```js
/**
 * Duration before a killstreak expires (defaults to never)
 * @type {number}
 */
killstreakDuration = 200000000
```

---

<div align="left">
    <h3>〔 <code><b>damage</b></code> 〕</h3> 
</div>

<a id="dealingdamagemultiplier"></a>

```js
/**
 * Damage multiplier for all types of outgoing damage
 * @type {number}
 */
dealingDamageMultiplier = 1
```

<a id="dealingdamageheadmultiplier"></a>

```js
/**
 * Damage multiplier for head hits (guns)
 * @type {number}
 */
dealingDamageHeadMultiplier = 1.75
```

<a id="dealingdamagelegmultiplier"></a>

```js
/**
 * Damage multiplier for leg hits (guns)
 * @type {number}
 */
dealingDamageLegMultiplier = 1
```

<a id="dealingdamagedefaultmultiplier"></a>

```js
/**
 * Multiplier when hitting neither leg nor head (guns)
 * @type {number}
 */
dealingDamageDefaultMultiplier = 1
```

<a id="receivingdamagemultiplier"></a>

```js
/**
 * Damage multiplier for all types of incoming damage
 * @type {number}
 */
receivingDamageMultiplier = 1
```

<a id="falldamage"></a>

```js
/**
 * Whether to deal damage to the player when they fall
 * @type {boolean}
 */
fallDamage = false
```

<a id="stompdamagemultiplier"></a>

```js
/**
 * Multiplier for stomp damage (Spiked Boots)
 * @type {number}
 */
stompDamageMultiplier = 0
```

<a id="stompdamageradius"></a>

```js
/**
 * Radius affected by stomp damage
 * @type {number}
 */
stompDamageRadius = 0
```

---

<div align="left">
    <h3>〔 <code><b>knockback</b></code> 〕</h3> 
</div>

<a id="horizontalknockbackmultiplier"></a>

```js
/**
 * Multiplier for horizontal knockback when dealing damage
 * @type {number}
 */
horizontalKnockbackMultiplier = 1
```

<a id="verticalknockbackmultiplier"></a>

```js
/**
 * Multiplier for vertical knockback when dealing damage
 * @type {number}
 */
verticalKnockbackMultiplier = 1
```

---

<div align="left">
    <h3>〔 <code><b>kart</b></code> 〕</h3> 
</div>

<a id="karttargetspeedmult"></a>

```js
/**
 * Speed multiplier for karts
 * @type {number}
 */
kartTargetSpeedMult = 1
```

<a id="kartspeedeffectmult"></a>

```js
/**
 * Speed multiplier for speed boost effects in karts
 * @type {number}
 */
kartSpeedEffectMult = 1
```

<a id="kartglidertargetheight"></a>

```js
/**
 * Kart gliding height
 * @type {number}
 */
kartGliderTargetHeight = 25
```

<a id="kartgroundheight"></a>

```js
/**
 * Kart ground height
 * @type {number}
 */
kartGroundHeight = 4
```

<a id="kartapproachmaxspeedscalar"></a>

```js
/**
 * How much to step towards target speed each movement tick (acceleration)
 * @type {number}
 */
kartApproachMaxSpeedScalar = 1
```

---

<div align="left">
    <h3>〔 <code><b>friction</b></code> 〕</h3> 
</div>

<a id="airfrictionscale"></a>

```js
/**
 * Friction to apply to airborne players
 * @type {number}
 */
airFrictionScale = 1
```

<a id="groundfrictionscale"></a>

```js
/**
 * Friction to apply to grounded players
 * @type {number}
 */
groundFrictionScale = 1
```

<a id="airaccscale"></a>

```js
/**
 * Acceleration to apply to airborne players
 * @type {number}
 */
airAccScale = 1
```

<a id="airmomentumconservation"></a>

```js
/**
 * Whether to allow strafe + conserve momentum while airborne
 * @type {boolean}
 */
airMomentumConservation = false
```

---

<div align="left">
    <h3>〔 <code><b>aura</b></code> 〕</h3> 
</div>

<a id="auraperlevel"></a>

```js
/**
 * How much Aura XP is required per level
 * @type {number}
 */
auraPerLevel = 100
```

<a id="maxauralevel"></a>

```js
/**
 * Maximum Aura Level attainable (set to 0 to disable Aura XP)
 * @type {number}
 */
maxAuraLevel = 0
```

---

<div align="left">
    <h3>〔 <code><b>misc</b></code> 〕</h3> 
</div>

<a id="crouchmobdetectionradiusmultiplier"></a>

```js
/**
 * Multiplier for mob detection radius while crouching
 * @type {number}
 */
crouchMobDetectionRadiusMultiplier = 2
```

<a id="chatchannels"></a>

```js
/**
 * Allows selecting a channel passed to onPlayerChat
 * @type {{ channelName: string; elementContent: string | CustomTextStyling; elementBgColor: string; }[] | null}
 */
chatChannels = null
```

<a id="droppeditemscale"></a>

```js
/**
 * Scale factor to use for dropped item meshes
 * @type {number}
 */
droppedItemScale = 1
```

<a id="movementbasedfovscale"></a>

```js
/**
 * Amount player camera is affected by movement-based FOV
 * @type {number}
 */
movementBasedFovScale = 1
```

<a id="creative"></a>

```js
/**
 * Whether the player is in creative mode
 * @type {boolean}
 */
creative = false
```

<a id="compasstarget"></a>

```js
/**
 * The target the compass will point towards
 * @type {string | number | number[]}
 */
compassTarget = [0, 0, 0]
```

<a id="skybox"></a>

```js
/**
 * Skybox option (recommended to keep "default")
 * @type {string | EarthSkyBox}
 */
skyBox = "default"
```

<a id="defaultblock"></a>

```js
/**
 * Default block the player can change blocks to (used if canChange is true but useInventory is false)
 * @type {string}
 */
defaultBlock = "Block of Gold"
```

<a id="ttbmultiplier"></a>

```js
/**
 * Multiplier for the time to break any block
 * @type {number}
 */
ttbMultiplier = 1
```

<a id="strictfluidbuckets"></a>

```js
/**
 * Whether a player can place fluid when canChange is false
 * @type {boolean}
 */
strictFluidBuckets = true
```

---

<a id="extra-info"></a>

<div align="center">
	<h2>❮ <code><b>Extra Info</b></code> ❯</h2>
</div>

```ts
type CustomTextStyling = (string | EntityName | TranslatedText | StyledIcon | StyledText)[]
```

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
type TranslatedText = {
	translationKey: string
	params?: Record<string, string | number | boolean | EntityName>
}
```

```ts
type EarthSkyBox = {
	type: "earth"
	inclination?: number
	turbidity?: number
	infiniteDistance?: number
	luminance?: number
	yCameraOffset?: number
	azimuth?: number
	// Not part of sky model by default; heavily tint to a vertex color
	vertexTint?: [number, number, number]
}
```

```js
sky_box_options = [
	default,
	earth,
	interstellar,
	space_lightblue,
	space_blue,
	space_red,
	underwater,
];
```

---
