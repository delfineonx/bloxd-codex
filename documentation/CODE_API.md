
---

<div align="center">
  <h1>CODE API</h1>
  <p>
    <a href="#intro"><kbd>Intro</kbd></a> &nbsp;•&nbsp; 
    <a href="#methods"><kbd>Methods</kbd></a> &nbsp;•&nbsp; 
    <a href="#reference"><kbd>Reference</kbd></a>
  </p>
</div>

---

<a id="intro"></a>
<details open>
  <summary>
    <div align="center">
      <h2>❮ <code><b>Intro</b></code> ❯</h2>
    </div>
  </summary>

> <h3><code><b>! IMPORTANT</b></code></h3>
> <code>api</code> is global object (i.e. <code>globalThis.api</code>).<br>
> <code>It has fields and methods (described below) which are:</code><br>
> <ul>
>   <li><a href="https://javascript.info/property-descriptors#non-writable"><code>non-writable</code></a> — read-only (cannot be reassigned)</li>
>   <li><a href="https://javascript.info/property-descriptors#non-enumerable"><code>non-enumerable</code></a> — not listed in loops (e.g. <code>for..in</code>)</li>
>   <li><a href="https://javascript.info/property-descriptors#non-configurable"><code>non-configurable</code></a> — cannot be deleted, and its attributes cannot be modified</li>
> </ul>

> <h3><code><b>! NOTE</b></code></h3>
> <ul>
>   <li><b><code>globalThis.myId</code></b>/<b><code>api.myId</code></b> and <b><code>globalThis.playerId</code></b>/<b><code>api.playerId</code></b> store the player id of who is executing the code block. It cannot be used the same way in <code>World Code</code>.</li>
>   <li><b><code>globalThis.thisPos</code></b>/<b><code>api.thisPos</code></b> stores the possition array <code>[x, y, z]</code> of the currently executing code block. It cannot be used the same way in <code>World Code</code>.</li>
>   <li><b><code>api.ownerDbId</code></b> stores the permanent (database) identifier of the world/lobby owner.</li>
>   <li>You can use <b><code>api.log()</code></b> or <b><code>console.log()</code></b> for printing and debugging (they do the same thing).</li>
>   <li>You can use <b><code>Date.now()</code></b> or <b><code>api.now()</code></b> — both return cached (~50 ms quantized) time in milliseconds.</li>
>   <li>Comments like <b><code>/* comment */</code></b> and <b><code>// comment</code></b> work.</li>
> </ul>

</details>

---

<a id="methods"></a>
<details open>
  <summary>
    <div align="center">
      <h2>❮ <code><b>Methods</b></code> ❯</h2>
    </div>
  </summary>

> <h3><code><b>! NOTE</b></code></h3>
> <code>"lifeform" means either player or mob.</code><br>
> <code>"entity" could be player, mob, dropped item or mesh.</code><br>
> <code>Some API methods may work correctly not with every entity type (mostly they are listed).</code><br>
> <code>"EntityId", "LifeformId", "PlayerId", "MobId" are always strings that represent negative numbers.</code><br>

<div align="center">
  <table>
    <tbody>
      <tr>
        <td valign="top" align="left">
          <h4 align="center"><code>player functions</code></h4>
          <div align="left">
            <a href="#getplayerids"><code>getPlayerIds</code></a><br>
            <a href="#getnumplayers"><code>getNumPlayers</code></a><br>
            <a href="#ismobile"><code>isMobile</code></a><br>
            <a href="#playerisloggedin"><code>playerIsLoggedIn</code></a><br>
            <a href="#playerisingame"><code>playerIsInGame</code></a><br>
            <a href="#getplayerpartywhenjoined"><code>getPlayerPartyWhenJoined</code></a><br>
            <a href="#getplayerid"><code>getPlayerId</code></a><br>
            <a href="#getplayerdbid"><code>getPlayerDbId</code></a><br>
            <a href="#getplayeridfromdbid"><code>getPlayerIdFromDbId</code></a><br>
            <a href="#kickplayer"><code>kickPlayer</code></a><br>
            <a href="#isplayercrouching"><code>isPlayerCrouching</code></a><br>
            <a href="#forcerespawn"><code>forceRespawn</code></a><br>
            <a href="#getcurrentkillstreak"><code>getCurrentKillstreak</code></a><br>
            <a href="#clearkillstreak"><code>clearKillstreak</code></a><br>
            <a href="#setcamerazoom"><code>setCameraZoom</code></a><br>
            <a href="#setcameradirection"><code>setCameraDirection</code></a><br>
            <a href="#getplayertargetinfo"><code>getPlayerTargetInfo</code></a><br>
            <a href="#getplayerfacinginfo"><code>getPlayerFacingInfo</code></a><br>
            <a href="#getaurainfo"><code>getAuraInfo</code></a><br>
            <a href="#settotalaura"><code>setTotalAura</code></a><br>
            <a href="#setauralevel"><code>setAuraLevel</code></a><br>
            <a href="#applyaurachange"><code>applyAuraChange</code></a><br>
            <a href="#setplayerpose"><code>setPlayerPose</code></a><br>
            <a href="#setplayerphysicsstate"><code>setPlayerPhysicsState</code></a><br>
            <a href="#getplayerphysicsstate"><code>getPlayerPhysicsState</code></a><br>
            <a href="#changeplayerintoskin"><code>changePlayerIntoSkin</code></a><br>
            <a href="#removeappliedskin"><code>removeAppliedSkin</code></a><br>
            <a href="#playsound"><code>playSound</code></a><br>
            <a href="#broadcastsound"><code>broadcastSound</code></a><br>
            <a href="#playclientpredictedsound"><code>playClientPredictedSound</code></a><br>
            <a href="#broadcastmessage"><code>broadcastMessage</code></a><br>
            <a href="#sendmessage"><code>sendMessage</code></a><br>
            <a href="#sendflyingmiddlemessage"><code>sendFlyingMiddleMessage</code></a><br>
            <a href="#sendtoprighthelper"><code>sendTopRightHelper</code></a><br>
            <a href="#progressbarupdate"><code>progressBarUpdate</code></a><br>
            <a href="#initiatemiddlescreenbar"><code>initiateMiddleScreenBar</code></a><br>
            <a href="#removemiddlescreenbar"><code>removeMiddleScreenBar</code></a><br>
            <a href="#openshop"><code>openShop</code></a><br>
            <a href="#sendovershopinfo"><code>sendOverShopInfo</code></a><br>
            <a href="#showshoptutorial"><code>showShopTutorial</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>items functions</code></h4>
          <div align="left">
            <a href="#giveitem"><code>giveItem</code></a><br>
            <a href="#removeitemname"><code>removeItemName</code></a><br>
            <a href="#setitemslot"><code>setItemSlot</code></a><br>
            <a href="#getitemslot"><code>getItemSlot</code></a><br>
            <a href="#gethelditem"><code>getHeldItem</code></a><br>
            <a href="#hasitem"><code>hasItem</code></a><br>
            <a href="#getinventoryitemamount"><code>getInventoryItemAmount</code></a><br>
            <a href="#setselectedinventorysloti"><code>setSelectedInventorySlotI</code></a><br>
            <a href="#getselectedinventorysloti"><code>getSelectedInventorySlotI</code></a><br>
            <a href="#getinventoryfreeslotcount"><code>getInventoryFreeSlotCount</code></a><br>
            <a href="#inventoryisfull"><code>inventoryIsFull</code></a><br>
            <a href="#clearinventory"><code>clearInventory</code></a><br>
            <a href="#canopenstandardchest"><code>canOpenStandardChest</code></a><br>
            <a href="#givestandardchestitem"><code>giveStandardChestItem</code></a><br>
            <a href="#getstandardchestfreeslotcount"><code>getStandardChestFreeSlotCount</code></a><br>
            <a href="#getstandardchestitemamount"><code>getStandardChestItemAmount</code></a><br>
            <a href="#getstandardchestitemslot"><code>getStandardChestItemSlot</code></a><br>
            <a href="#getstandardchestitems"><code>getStandardChestItems</code></a><br>
            <a href="#setstandardchestitemslot"><code>setStandardChestItemSlot</code></a><br>
            <a href="#getmoonstonechestitemslot"><code>getMoonstoneChestItemSlot</code></a><br>
            <a href="#getmoonstonechestitems"><code>getMoonstoneChestItems</code></a><br>
            <a href="#setmoonstonechestitemslot"><code>setMoonstoneChestItemSlot</code></a><br>
            <a href="#edititemcraftingrecipes"><code>editItemCraftingRecipes</code></a><br>
            <a href="#resetitemcraftingrecipes"><code>resetItemCraftingRecipes</code></a><br>
            <a href="#removeitemcraftingrecipes"><code>removeItemCraftingRecipes</code></a><br>
            <a href="#createitemdrop"><code>createItemDrop</code></a><br>
            <a href="#setitemamount"><code>setItemAmount</code></a><br>
            <a href="#deleteitemdrop"><code>deleteItemDrop</code></a><br>
            <a href="#setcantpickupitem"><code>setCantPickUpItem</code></a><br>
            <a href="#getinitialitemmetadata"><code>getInitialItemMetadata</code></a><br>
            <a href="#getitemstat"><code>getItemStat</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>entity functions</code></h4>
          <div align="left">
            <a href="#checkvalid"><code>checkValid</code></a><br>
            <a href="#isalive"><code>isAlive</code></a><br>
            <a href="#getentityname"><code>getEntityName</code></a><br>
            <a href="#getentitytype"><code>getEntityType</code></a><br>
            <a href="#getentitiesinrect"><code>getEntitiesInRect</code></a><br>
            <a href="#getposition"><code>getPosition</code></a><br>
            <a href="#setposition"><code>setPosition</code></a><br>
            <a href="#getvelocity"><code>getVelocity</code></a><br>
            <a href="#setvelocity"><code>setVelocity</code></a><br>
            <a href="#applyimpulse"><code>applyImpulse</code></a><br>
            <a href="#setentityheading"><code>setEntityHeading</code></a><br>
            <a href="#getblockcoordinatesplayerstandingon"><code>getBlockCoordinatesPlayerStandingOn</code></a><br>
            <a href="#getblocktypesplayerstandingon"><code>getBlockTypesPlayerStandingOn</code></a><br>
            <a href="#getunitcoordinateslifeformwithin"><code>getUnitCoordinatesLifeformWithin</code></a><br>
            <a href="#getshieldamount"><code>getShieldAmount</code></a><br>
            <a href="#setshieldamount"><code>setShieldAmount</code></a><br>
            <a href="#gethealth"><code>getHealth</code></a><br>
            <a href="#sethealth"><code>setHealth</code></a><br>
            <a href="#applyhealthchange"><code>applyHealthChange</code></a><br>
            <a href="#applymeleehit"><code>applyMeleeHit</code></a><br>
            <a href="#attemptapplydamage"><code>attemptApplyDamage</code></a><br>
            <a href="#killlifeform"><code>killLifeform</code></a><br>
            <a href="#applyeffect"><code>applyEffect</code></a><br>
            <a href="#geteffects"><code>getEffects</code></a><br>
            <a href="#removeeffect"><code>removeEffect</code></a><br>
            <a href="#scaleplayermeshnodes"><code>scalePlayerMeshNodes</code></a><br>
            <a href="#updateentitynodemeshattachment"><code>updateEntityNodeMeshAttachment</code></a><br>
            <a href="#addfollowingentitytoplayer"><code>addFollowingEntityToPlayer</code></a><br>
            <a href="#removefollowingentityfromplayer"><code>removeFollowingEntityFromPlayer</code></a><br>
            <a href="#calcexplosionforce"><code>calcExplosionForce</code></a><br>
          </div>
        </td>
      </tr>
      <tr>
        <td valign="top" align="left">
          <h4 align="center"><code>block functions</code></h4>
          <div align="left">
            <a href="#getblock"><code>getBlock</code></a><br>
            <a href="#getblockid"><code>getBlockId</code></a><br>
            <a href="#setblock"><code>setBlock</code></a><br>
            <a href="#attemptworldchangeblock"><code>attemptWorldChangeBlock</code></a><br>
            <a href="#setblockrect"><code>setBlockRect</code></a><br>
            <a href="#setblockwalls"><code>setBlockWalls</code></a><br>
            <a href="#setblockdata"><code>setBlockData</code></a><br>
            <a href="#getblockdata"><code>getBlockData</code></a><br>
            <a href="#isblockinloadedchunk"><code>isBlockInLoadedChunk</code></a><br>
            <a href="#getblocksolidity"><code>getBlockSolidity</code></a><br>
            <a href="#getmetainfo"><code>getMetaInfo</code></a><br>
            <a href="#blocknametoblockid"><code>blockNameToBlockId</code></a><br>
            <a href="#blockidtoblockname"><code>blockIdToBlockName</code></a><br>
            <a href="#blockcoordtochunkid"><code>blockCoordToChunkId</code></a><br>
            <a href="#chunkidtobotleftcoord"><code>chunkIdToBotLeftCoord</code></a><br>
            <a href="#setcanchangeblock"><code>setCanChangeBlock</code></a><br>
            <a href="#setcantchangeblock"><code>setCantChangeBlock</code></a><br>
            <a href="#setcanchangeblocktype"><code>setCanChangeBlockType</code></a><br>
            <a href="#setcantchangeblocktype"><code>setCantChangeBlockType</code></a><br>
            <a href="#resetcanchangeblocktype"><code>resetCanChangeBlockType</code></a><br>
            <a href="#setcanchangeblockrect"><code>setCanChangeBlockRect</code></a><br>
            <a href="#setcantchangeblockrect"><code>setCantChangeBlockRect</code></a><br>
            <a href="#resetcanchangeblockrect"><code>resetCanChangeBlockRect</code></a><br>
            <a href="#setwalkthroughtype"><code>setWalkThroughType</code></a><br>
            <a href="#setwalkthroughrect"><code>setWalkThroughRect</code></a><br>
            <a href="#raycastforblock"><code>raycastForBlock</code></a><br>
            <a href="#playparticleeffect"><code>playParticleEffect</code></a><br>
            <a href="#isinsiderect"><code>isInsideRect</code></a><br>
            <a href="#getchunk"><code>getChunk</code></a><br>
            <a href="#getemptychunk"><code>getEmptyChunk</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>mob functions</code></h4>
          <div align="left">
            <a href="#getnummobs"><code>getNumMobs</code></a><br>
            <a href="#getmobids"><code>getMobIds</code></a><br>
            <a href="#createmobherd"><code>createMobHerd</code></a><br>
            <a href="#attemptspawnmob"><code>attemptSpawnMob</code></a><br>
            <a href="#despawnmob"><code>despawnMob</code></a><br>
            <a href="#getdefaultmobsetting"><code>getDefaultMobSetting</code></a><br>
            <a href="#setdefaultmobsetting"><code>setDefaultMobSetting</code></a><br>
            <a href="#getmobsetting"><code>getMobSetting</code></a><br>
            <a href="#setmobsetting"><code>setMobSetting</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>entity settings</code></h4>
          <div align="left">
            <a href="#setotherentitysetting"><code>setOtherEntitySetting</code></a><br>
            <a href="#setotherentitysettings"><code>setOtherEntitySettings</code></a><br>
            <a href="#getotherentitysetting"><code>getOtherEntitySetting</code></a><br>
            <a href="#settargetedplayersettingforeveryone"><code>setTargetedPlayerSettingForEveryone</code></a><br>
            <a href="#seteveryonesettingforplayer"><code>setEveryoneSettingForPlayer</code></a><br>
            <a href="#setplayeropacity"><code>setPlayerOpacity</code></a><br>
            <a href="#setplayeropacityforoneplayer"><code>setPlayerOpacityForOnePlayer</code></a><br>
          </div>
        </td>
      </tr>
      <tr>
        <td valign="top" align="left">
          <h4 align="center"><code>lobby functions</code></h4>
          <div align="left">
            <a href="#now"><code>now</code></a><br>
            <a href="#getlobbyname"><code>getLobbyName</code></a><br>
            <a href="#ispubliclobby"><code>isPublicLobby</code></a><br>
            <a href="#getlobbytype"><code>getLobbyType</code></a><br>
            <a href="#setmaxplayers"><code>setMaxPlayers</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>client options</code></h4>
          <div align="left">
            <a href="#setclientoption"><code>setClientOption</code></a><br>
            <a href="#getclientoption"><code>getClientOption</code></a><br>
            <a href="#setclientoptions"><code>setClientOptions</code></a><br>
            <a href="#setclientoptiontodefault"><code>setClientOptionToDefault</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>callback functions</code></h4>
          <div align="left">
            <a href="#setcallbackvaluefallback"><code>setCallbackValueFallback</code></a><br>
          </div>
        </td>
      </tr>
    </tbody>
  </table>
</div>

---

<div align="left">
  <h3>〔 <code><b>entity functions</b></code> 〕</h3>
</div>

<a id="checkvalid"></a>

```js
/**
 * Check an entity (player / mob / item / mesh) is still valid and executing.
 *
 * @param {EntityId} [entityId]
 * @returns {boolean}
 */
checkValid(entityId)
```

<a id="isalive"></a>

```js
/**
 * Whether a lifeform is alive or dead (or on the respawn screen, in a player's case).
 *
 * @param {LifeformId} lifeformId
 * @returns {boolean}
 */
isAlive(lifeformId)
```

<a id="getentityname"></a>

```js
/**
 * Get the in game name of an entity (player / mob / item / mesh).
 *
 * @param {EntityId} entityId
 * @returns {string}
 */
getEntityName(entityId)
```

<a id="getentitytype"></a>

```js
/**
 * Get the type of an entity ("Player" / "MobType" / "Item" / "Mesh").
 * 
 * @param {EntityId} entityId
 * @returns {EntityType}
 */
getEntityType(entityId)
```

<a id="getentitiesinrect"></a>

```js
/**
 * Get the entities (players, mobs, items, meshes) in the rect between [minX, minY, minZ] and [maxX, maxY, maxZ]
 *
 * @param {[number, number, number]} minCoords
 * @param {[number, number, number]} maxCoords
 * @returns {EntityId[]}
 */
getEntitiesInRect(minCoords, maxCoords)
```

<a id="getposition"></a>

```js
/**
 * Get the position of an enitity (player / mob / item / mesh).
 *
 * @param {EntityId} entityId
 * @returns {[number, number, number]} - [x, y, z]
 */
getPosition(entityId)
```

<a id="setposition"></a>

```js
/**
 * Set the position of an enitity (player / mob / item / mesh).
 *
 * @param {EntityId} entityId
 * @param {number | [number, number, number]} x - Could be an array [x, y, z]. If so, the other params shouldn't be passed.
 * @param {number} [y]
 * @param {number} [z]
 * @returns {void}
 */
setPosition(entityId, x, y, z)
```

<a id="getvelocity"></a>

```js
/**
 * Get the velocity of an enitity (player / mob / item / mesh).
 *
 * @param {EntityId} entityId
 * @returns {[number, number, number]} - [x, y, z]
 */
getVelocity(entityId)
```

<a id="setvelocity"></a>

```js
/**
 * Set the velocity of an enitity (player / mob / mesh).
 *
 * @param {EntityId} entityId
 * @param {number} x
 * @param {number} y
 * @param {number} z
 * @returns {void}
 */
setVelocity(entityId, x, y, z)
```

<a id="applyimpulse"></a>

```js
/**
 * Apply an impulse to an entity (player / mob / item / mesh).
 *
 * @param {EntityId} entityId
 * @param {number} xImpulse
 * @param {number} yImpulse
 * @param {number} zImpulse
 * @returns {void}
 */
applyImpulse(entityId, xImpulse, yImpulse, zImpulse)
```

<a id="setentityheading"></a>

```js
/**
 * Set the heading for a server-auth entity.
 *
 * @param {EntityId} entityId
 * @param {number} newHeading - Radians
 * @returns {void}
 */
setEntityHeading(entityId, newHeading)
```

<a id="getblockcoordinatesplayerstandingon"></a>

```js
/**
 * Get the coordinates of the blocks the entity (player / mob / item / mesh) is standing on as a list.
 * 
 * Example:
 * If the center of the entity is at [0, 0, 0], the function will return [[0, -1, 0], [-1, -1, 0], [0, -1, -1], [-1, -1, -1]]
 * If the entity is just standing on one block, the function would return e.g. [[0, 0, 0]]
 * If the entity is middair then returns an empty array [].
 *
 * @param {EntityId} entityId
 * @returns {number[][]}
 */
getBlockCoordinatesPlayerStandingOn(entityId)
```

<a id="getblocktypesplayerstandingon"></a>

```js
/**
 * Get the types of block the entity (player / mob / item / mesh) is standing on.
 *
 * Example: (similar to `getBlockCoordinatesPlayerStandingOn()`)
 * If the entity is standing on 4 dirt blocks, this will return ["Dirt", "Dirt", "Dirt", "Dirt"]
 * If the entity is middair then returns an empty array [].
 *
 * @param {EntityId} entityId
 * @returns {any[]}
 */
getBlockTypesPlayerStandingOn(entityId)
```

<a id="getunitcoordinateslifeformwithin"></a>

```js
/**
 * Get the up to 12 unit coordinates the lifeform/entity (player / mob / item / mesh) is located within.
 * A lifeform/entity is modeled as having four corners.
 *
 * @param {EntityId} entityId
 * @returns {number[][]} - List of [x, y, z] positions.
 */
getUnitCoordinatesLifeformWithin(entityId)
```

<a id="getshieldamount"></a>

```js
/**
 * Get the current shield of an entity.
 *
 * @param {EntityId} entityId
 * @returns {number}
 */
getShieldAmount(entityId)
```

<a id="setshieldamount"></a>

```js
/**
 * Set the current shield of a lifeform.
 * The targeted lifeform has to have non-null health.
 *
 * @param {LifeformId} lifeformId
 * @param {number} newShieldAmount - Must be non-negative integer
 * @returns {void}
 */
setShieldAmount(lifeformId, newShieldAmount)
```

<a id="gethealth"></a>

```js
/**
 * Get the current health of an entity.
 *
 * @param {LifeformId} lifeformId
 * @returns {number}
 */
getHealth(lifeformId)
```

<a id="sethealth"></a>

```js
/**
 * Set the current health of a lifeform.
 * If you want to set their health to more than their current max health (or change from `null`), the optional `increaseMaxHealthIfNeeded` must be true.
 *
 * @param {LifeformId} lifeformId
 * @param {number | null} newHealth - Must be non-negative integer. `null` makes the lifeform not to have health
 * @param { LifeformId | { lifeformId: LifeformId, withItem: string } } [whoDidDamage]
 * @param {boolean} [increaseMaxHealthIfNeeded]
 * @returns {boolean} - Whether this change in health killed the lifeform
 */
setHealth(lifeformId, newHealth, whoDidDamage, increaseMaxHealthIfNeeded)
```

<a id="applyhealthchange"></a>

```js
/**
 * @param {LifeformId} lifeformId
 * @param {number} changeAmount - Must be integer. A positive amount will increase the entity's health. A negative amount will decrease the entity's shield first, then their health.
 * @param { LifeformId | { lifeformId: LifeformId; withItem: string } } [whoDidDamage]
 * @param {boolean} [broadcastLifeformHurt]
 * @returns {boolean} - Whether this change in health killed the lifeform
 */
applyHealthChange(lifeformId, changeAmount, whoDidDamage, broadcastLifeformHurt)

```

<a id="applymeleehit"></a>

```js
/**
 * Make it as if initiatorEntityId hit hitEntityId.
 *
 * @param {LifeformId} initiatorEntityId
 * @param {LifeformId} hitEntityId
 * @param {[number, number, number]} dirFacing - direction unit vector
 * @param {PNull<PlayerBodyPart>} [bodyPartHit]
 * @param { {
 *   damage?: PNull<number>
 *   heldItemName?: PNull<string>
 *   horizontalKbMultiplier?: number
 *   verticalKbMultiplier?: number
 * } } [overrides]
 * @returns {boolean}
 */
applyMeleeHit(initiatorEntityId, hitEntityId, dirFacing, bodyPartHit, overrides)
```

<a id="attemptapplydamage"></a>

```js
/**
 * Apply damage to a lifeform.
 * It is recommended to self-inflict damage when the game code wants to apply damage to a lifeform.
 *
 * @param {PlayerAttemptDamageOtherPlayerOptions} {
 *   initiatorEntityId,
 *   hitEntityId,
 *   attemptedDamageAmount,
 *   withItem,
 *   bodyPartHit = undefined,
 *   attackDir = undefined,
 *   showCritParticles = false,
 *   reduceVerticalKbVelocity = true,
 *   horizontalKbMultiplier = 1,
 *   verticalKbMultiplier = 1,
 *   broadcastEntityHurt = true,
 *   attackCooldownSettings = null,
 *   hittingSoundOverride = null,
 *   ignoreOtherEntitySettingCanAttack = false,
 *   isTrueDamage = false,
 *   damagerDbId = null,
 * }
 * @returns {boolean} - whether the attack damaged the lifeform
 */
attemptApplyDamage({
  initiatorEntityId,
  hitEntityId,
  attemptedDamageAmount,
  withItem,
  bodyPartHit = undefined,
  attackDir = undefined,
  showCritParticles = false,
  reduceVerticalKbVelocity = true,
  horizontalKbMultiplier = 1,
  verticalKbMultiplier = 1,
  broadcastEntityHurt = true,
  attackCooldownSettings = null,
  hittingSoundOverride = null,
  ignoreOtherEntitySettingCanAttack = false,
  isTrueDamage = false,
  damagerDbId = null,
})
```

<a id="killlifeform"></a>

```js
/**
 * Kill a lifeform.
 *
 * @param {LifeformId} lifeformId
 * @param { LifeformId | { lifeformId: LifeformId, withItem: string } } [whoKilled]
 * @returns {void}
 */
killLifeform(lifeformId, whoKilled)
```

<a id="applyeffect"></a>

```js
/**
 * Apply an effect to a lifeform.
 * 
 * Can be an inbuilt effect, e.g. "Speed" (speed boost), "Damage" (damage boost).
 * For inbuilt just pass the name of the effect and the functionality is handled by engine.
 *
 * For custom effect, you pass customEffectInfo. The icon can be an icon from "IngameIcons.ts" or a bloxd item name.
 * The custom effect `onEndCb` is an optional helper within which you can undo the effect you applied.
 * 
 * Note that `onEndCb` will not work for press to code boards, code blocks or world code.
 *
 * @param {LifeformId} lifeformId
 * @param {string} effectName
 * @param {number | null} duration
 * @param { { icon?: IngameIconName | ItemName, displayName?: string | TranslatedText, onEndCb?: () => void } & Partial<InbuiltEffectInfo> } customEffectInfo
 * @returns {void}
 */
applyEffect(lifeformId, effectName, duration, customEffectInfo)
```

<a id="geteffects"></a>

```js
/**
 * Get all the effects currently applied to a lifeform.
 *
 * @param {LifeformId} lifeformId
 * @returns {string[]}
 */
getEffects(lifeformId)
```

<a id="removeeffect"></a>

```js
/**
 * Remove an effect from a lifeform.
 *
 * @param {LifeformId} lifeformId
 * @param {string} effectName
 * @returns {void}
 */
removeEffect(lifeformId, effectName)
```

<a id="scaleplayermeshnodes"></a>

```js
/**
 * Scale node of a lifeform's mesh by 3d vector.
 * State from prior calls to this api is lost, so if you want to have multiple nodes scaled, pass in all the scales at once.
 *
 * @param {LifeformId} lifefromId - player or mob
 * @param {EntityMeshScalingMap} nodeScales
 * @returns {void}
 */
scalePlayerMeshNodes(lifefromId, nodeScales)
```

<a id="updateentitynodemeshattachment"></a>

```js
/**
 * Attach/detach mesh instances to/from an entity (player / mob).
 *
 * @param {EntityId} entityId
 * @param {EntityNamedNode} node - node to attach to
 * @param {MeshType|null} type - if null, detaches mesh from this node
 * @param {MeshEntityOptions[MeshType]} [options]
 * @param {[number, number, number]} [offset]
 * @param {[number, number, number]} [rotation]
 * @returns {void}
 */
updateEntityNodeMeshAttachment(entityId, node, type, options, offset, rotation)
```

<a id="addfollowingentitytoplayer"></a>

```js
/**
 * Add following entity to the targeted entity.
 *
 * targetedEntityId is player -> followingEntityId is mob / mesh
 * targetedEntityId is mob    -> followingEntityId is mob / mesh
 * targetedEntityId is item   -> followingEntityId is mob / mesh
 * targetedEntityId is mesh   -> followingEntityId is mob / mesh
 *
 * @param {EntityId} targetedEntityId
 * @param {EntityId} followingEntityId
 * @param {[number, number, number]} [offset]
 * @returns {void}
 */
addFollowingEntityToPlayer(targetedEntityId, followingEntityId, offset)
```

<a id="removefollowingentityfromplayer"></a>

```js
/**
 * Remove following entity from the targeted entity.
 *
 * @param {EntityId} targetedEntityId
 * @param {EntityId} followingEntityId
 * @returns {void}
 */
removeFollowingEntityFromPlayer(targetedEntityId, followingEntityId)
```

<a id="calcexplosionforce"></a>

```js
/**
 * Calculates explosion force, and does NOT make an actual explosion.
 * 
 * @param {EntityId} entityId
 * @param {ExplosionType} explosionType
 * @param {number} knockbackFactor
 * @param {number} explosionRadius
 * @param {[number, number, number]} explosionPosition
 * @param {boolean} ignoreProjectiles
 * @returns { { force: [number, number, number], forceFrac: number } }
 */
calcExplosionForce(entityId, explosionType, knockbackFactor, explosionRadius, explosionPosition, ignoreProjectiles)
```

---

<div align="left">
  <h3>〔 <code><b>entity settings</b></code> 〕</h3>
</div>

<a id="setotherentitysetting"></a>

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

<a id="setotherentitysettings"></a>

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

<a id="getotherentitysetting"></a>

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

<a id="settargetedplayersettingforeveryone"></a>

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

<a id="seteveryonesettingforplayer"></a>

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

<a id="setplayeropacity"></a>

```js
/**
 * Set a lifefrom's opacity.
 * A simple helper that calls `setTargetedPlayerSettingForEveryone()`
 *
 * @param {LifeformId} lifefromId - player / mob
 * @param {number} opacity
 * @returns {void}
 */
setPlayerOpacity(lifefromId, opacity)
```

<a id="setplayeropacityforoneplayer"></a>

```js
/**
 * Set the level of viewable opacity by one player on another player.
 * A simple helper that calls `setOtherEntitySetting()`
 *
 * @param {PlayerId} playerIdWhoViewsOpacityPlayer - The player who sees that with opacity.
 * @param {PlayerId} playerIdOfOpacityPlayer - The player who is given opacity.
 * @param {number} opacity
 * @returns {void}
 */
setPlayerOpacityForOnePlayer(playerIdWhoViewsOpacityPlayer, playerIdOfOpacityPlayer, opacity)
```

---

<div align="left">
  <h3>〔 <code><b>player functions</b></code> 〕</h3>
</div>


<a id="getplayerids"></a>

```js
/**
 * Get all the player ids.
 *
 * @returns {PlayerId[]}
 */
getPlayerIds()
```

<a id="getnumplayers"></a>

```js
/**
 * Get the number of players in the lobby.
 *
 * @returns {number}
 */
getNumPlayers()
```

<a id="ismobile"></a>

```js
/**
 * Whether the player is on a mobile device or a computer.
 *
 * @param {PlayerId} playerId
 * @returns {boolean}
 */
isMobile(playerId)
```

<a id="playerisloggedin"></a>

```js
/**
 * Whether player's account is not in an anonymous state.
 *
 * @param {PlayerId} playerId
 * @returns {boolean}
 */
playerIsLoggedIn(playerId)
```

<a id="playerisingame"></a>

```js
/**
 * Whether a player is currently in the game.
 *
 * @param {PlayerId} playerId
 * @returns {boolean}
 */
playerIsInGame(playerId)
```

<a id="getplayerpartywhenjoined"></a>

```js
/**
 * Returns the party that the player was in when they joined the game.
 * The returned object contains the playerDbIds,
 * as well as the playerIds if available, of the party leader and members.
 *
 * @param {PlayerId} playerId
 * @returns { { playerDbIds: PlayerDbId[] } | null }
 */
getPlayerPartyWhenJoined(playerId)
```

<a id="getplayerid"></a>

```js
/**
 * Given the name of a player, get their id.
 *
 * @param {string} playerName
 * @returns { PlayerId | null }
 */
getPlayerId(playerName)
```

<a id="getplayerdbid"></a>

```js
/**
 * Given a player, get their permanent identifier that doesn't change when leaving and re-entering.
 *
 * @param {PlayerId} playerId
 * @returns {PlayerDbId}
 */
getPlayerDbId(playerId)
```

<a id="getplayeridfromdbid"></a>

```js
/**
 * Returns null if player is not in lobby.
 *
 * @param {PlayerDbId} dbId
 * @returns { PlayerId | null }
 */
getPlayerIdFromDbId(dbId)
```

<a id="kickplayer"></a>

```js
/**
 * Temporary kick player from a lobby.
 * 
 * @param {PlayerId} playerId
 * @param {string} reason - message
 * @returns {void}
 */
kickPlayer(playerId, reason)
```

<a id="isplayercrouching"></a>

```js
/**
 * Check whether a player is crouching.
 *
 * @param {PlayerId} playerId
 * @returns {boolean}
 */
isPlayerCrouching(playerId)
```

<a id="forcerespawn"></a>

```js
/**
 * Force respawn a player.
 *
 * @param {PlayerId} playerId
 * @param {[number, number, number]} [respawnPos]
 * @returns {void}
 */
forceRespawn(playerId, respawnPos)
```

<a id="getcurrentkillstreak"></a>

```js
/**
 * Gets the player's current killstreak.
 *
 * @param {PlayerId} playerId
 * @returns {number}
 */
getCurrentKillstreak(playerId)
```

<a id="clearkillstreak"></a>

```js
/**
 * Clears the player's current killstreak
 *
 * @param {PlayerId} playerId
 * @returns {void}
 */
clearKillstreak(playerId)
```

<a id="setcamerazoom"></a>

```js
/**
 * Set camera zoom for a player.
 *
 * @param {PlayerId} playerId
 * @param {number} zoom
 * @returns {void}
 */
setCameraZoom(playerId, zoom)
```

<a id="setcameradirection"></a>

```js
/**
 * Set the direction the player is looking.
 *
 * @param {PlayerId} playerId
 * @param {[number, number, number} direction - unit vector
 * @returns {void}
 */
setCameraDirection(playerId, direction)
```

<a id="getplayertargetinfo"></a>

```js
/**
 * Get the position of a player's target block and the block adjacent to it (e.g. where a block would be placed).
 * Range radius is limited to 6 voxels (blocks).
 *
 * @param {PlayerId} playerId
 * @returns { {
 *   position: [number, number, number],
 *   normal: [number, number, number],
 *   adjacent: [number, number, number],
 * } }
 */
getPlayerTargetInfo(playerId)
```

<a id="getplayerfacinginfo"></a>

```js
/**
 * Get the position of a player's camera and the direction (both in Euclidean and spherical coordinates).
 * 
 * `moveHeading` gives only camera (head) rotation, NOT body rotation - i.e. the same as `angleDir.phi`
 *
 * @param {PlayerId} playerId
 * @returns { {
 *   camPos: [number, number, number],
 *   dir: [number, number, number],
 *   angleDir: { theta: number, phi: number },
 *   moveHeading: number
 * } }
 */
getPlayerFacingInfo(playerId)
```

<a id="getaurainfo"></a>

```js
/**
 * Get the aura info for a player.
 *
 * @param {PlayerId} playerId
 * @returns { { level: number, totalAura: number, auraPerLevel: number } }
 */
getAuraInfo(playerId)
```

<a id="settotalaura"></a>

```js
/**
 * Sets the total aura for a player.
 * Will not go over max level or under 0.
 *
 * @param {PlayerId} playerId
 * @param {number} totalAura
 * @returns {void}
 */
setTotalAura(playerId, totalAura)
```

<a id="setauralevel"></a>

```js
/**
 * Set the aura level for a player - shortcut for `setTotalAura(level * auraPerLevel)`.
 *
 * @param {PlayerId} playerId
 * @param {number} level
 * @returns {void}
 */
setAuraLevel(playerId, level)
```

<a id="applyaurachange"></a>

```js
/**
 * Add (or remove if negative) aura to a player.
 * Will not go over max level or under 0.
 *
 * @param {PlayerId} playerId
 * @param {number} auraDiff
 * @returns {number} - The actual change in aura
 */
applyAuraChange(playerId, auraDiff)
```

<a id="setplayerpose"></a>

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

<a id="setplayerphysicsstate"></a>

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

<a id="getplayerphysicsstate"></a>

```js
/**
 * Get physics state for player.
 *
 * @param {PlayerId} playerId
 * @returns {PlayerPhysicsStateData}
 */
getPlayerPhysicsState(playerId)
```

<a id="changeplayerintoskin"></a>

```js
/**
 * Change a part of a player's skin.
 *
 * @param {PlayerId} playerId
 * @param {CosmeticType} cosmeticType - Type of cosmetic.
 * @param {CosmeticName} cosmeticName - Chosen cosmetic, will be made lowercase automatically.
 * @returns {void}
 */
changePlayerIntoSkin(playerId, cosmeticType, cosmeticName)
```

<a id="removeappliedskin"></a>

```js
/**
 * Remove gamemode-applied skin from a player.
 *
 * @param {PlayerId} playerId
 * @returns {void}
 */
removeAppliedSkin(playerId)
```

<a id="playsound"></a>

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

<a id="broadcastsound"></a>

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

<a id="playclientpredictedsound"></a>

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

<a id="broadcastmessage"></a>

```js
/**
 * Send a message to everyone in chat.
 *
 * @param {string | CustomTextStyling} message - The text contained within the message. Can use `Custom Text Styling`.
 * @param { { fontWeight?: number | string; color?: string } } [style]
 *   - An optional style argument.
 *   - Can contain values for fontWeight and color of the message.
 *   - `style` is ignored if message uses custom text styling (i.e. is not a string).
 * @returns {void}
 */
broadcastMessage(message, style)
```

<a id="sendmessage"></a>

```js
/**
 * Send a message to a specific player.
 *
 * @param {PlayerId} playerId
 * @param {string | CustomTextStyling} message - The text contained within the message. Can use `Custom Text Styling`.
 * @param { { fontWeight?: number | string; color?: string } } [style]
 *   - An optional style argument.
 *   - Can contain values for fontWeight and color of the message.
 *   - `style` is ignored if message uses custom text styling (i.e. is not a string).
 * @returns {void}
 */
sendMessage(playerId, message, style)
```

<a id="sendflyingmiddlemessage"></a>

```js
/**
 * Send a flying middle message to a specific player.
 *
 * @param {PlayerId} playerId
 * @param {CustomTextStyling} message - The text contained within the message. Can use `Custom Text Styling`.
 * @param {number} distanceFromAction
 *   - The distance from the action that has caused this message to be displayed.
 *   - This value will be used to determine how the message flies across the screen.
 * @returns {void}
 */
sendFlyingMiddleMessage(playerId, message, distanceFromAction)
```

<a id="sendtoprighthelper"></a>

```js
/**
 * @deprecated - prefer using other UI elements
 * (this UI element hasn't been properly thought through in combination with other elements like killfeed, uirequests, etc.)
 *
 * Send a player an icon in the top right corner.
 *
 * @param {PlayerId} playerId
 * @param {string} icon - Can be any icon from font-awesome.
 * @param {string} text - The text to send.
 * @param { {
 *   duration?: number
 *   width?: number
 *   height?: number
 *   color?: string
 *   iconSizeMult?: number
 *   textAndIconColor?: string
 *   fontSize?: string
 * } } options - Can include keys duration, width, height, color, iconSizeMult.
 * @returns {void}
 */
sendTopRightHelper(playerId, icon, text, options)
```

<a id="progressbarupdate"></a>

```js
/**
 * Update the progress bar in the bottom right corner.
 * Can be queued.
 *
 * @param {PlayerId} playerId
 * @param {number} toFraction - The fraction of the progress bar you want to be filled up.
 * @param {number} [toDuration]
 *   - The time it takes for the bar to reach the given toFraction in milliseconds.
 *   - If this is too low and you queue multiple updates, this toFraction could be skipped. Treat 200ms as a minimum.
 * @returns {void}
 */
progressBarUpdate(playerId, toFraction, toDuration)
```

<a id="initiatemiddlescreenbar"></a>

```js
/**
 * This will initiate the MiddleScreenBar, starting at empty and filling up to full over the given duration.
 * Good to represent cooldowns (e.g. gun reload) or charged items (e.g. crossbow).
 *
 * @param {PlayerId} playerId
 * @param {number} duration - milliseconds over which the MiddleScreenBar fills up.
 * @param {boolean} [chargeExpiresAutomatically]
 *   - Defaults to true.
 *   - If true, the bar will disappear upon reaching full.
 *   - If false, the bar will remain at full until hidden with removeMiddleScreenBar.
 * @param {number} [horizontalBarRemOffset] - Offset the bar left or right (in css unit - rem).
 * @returns {void}
 */
initiateMiddleScreenBar(playerId, duration, chargeExpiresAutomatically, horizontalBarRemOffset)
```

<a id="removemiddlescreenbar"></a>

```js
/**
 * If there is any current middle screen bar running, this will hide it.
 *
 * @param {PlayerId} playerId
 * @returns {void}
 */
removeMiddleScreenBar(playerId)
```

<a id="openshop"></a>

```js
/**
 * Open the shop UI for a player.
 *
 * @param {PlayerId} playerId
 * @param {boolean} [toggle] - Whether to close the shop if it's already open.
 * @param {string} [forceCategory] - If set, will change the shop to this category.
 * @returns {void}
 */
openShop(playerId, toggle, forceCategory)
```

<a id="sendovershopinfo"></a>

```js
/**
 * Show a message over the shop in the same place that a shop item's onBoughtMessage is shown.
 * Displays for a couple seconds before disappearing.
 * Use case is to show a dynamic message when player buys an item.
 *
 * @param {PlayerId} playerId
 * @param {string | CustomTextStyling} info
 * @returns {void}
 */
sendOverShopInfo(playerId, info)
```

<a id="showshoptutorial"></a>

```js
/**
 * Show the shop tutorial for a player.
 * Will not be shown if they have ever seen the shop tutorial in your game before.
 *
 * @param {PlayerId} playerId
 * @returns {void}
 */
showShopTutorial(playerId)
```

---

<div align="left">
  <h3>〔 <code><b>client options</b></code> 〕</h3>
</div>

<a id="setclientoption"></a>

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

<a id="getclientoption"></a>

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

<a id="setclientoptions"></a>

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

<a id="setclientoptiontodefault"></a>

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

<div align="left">
  <h3>〔 <code><b>mob functions</b></code> 〕</h3>
</div>

<a id="getnummobs"></a>

```js
/**
 * Get the number of mobs in the world.
 *
 * @returns {number}
 */
getNumMobs()
```

<a id="getmobids"></a>

```js
/**
 * Get the mob IDs of all mobs in the world.
 *
 * @returns {MobId[]}
 */
getMobIds()
```

<a id="createmobherd"></a>

```js
/**
 * Create a mob herd. 
 * A mob herd represents a collection of mobs that move together.
 *
 * @returns {MobHerdId} - Positive integer.
 */
createMobHerd()
```

<a id="attemptspawnmob"></a>

```js
/**
 * Try to spawn a mob into the world at a given position. Returns null on failure.
 * 
 * WARNING:
 * Either the "onPlayerAttemptSpawnMob" or the "onWorldAttemptSpawnMob" game callback will be called
 * depending on whether "spawnerId" is provided. Calling this function inside those callbacks risks infinite recursion.
 *
 * @param {TMobType} mobType
 * @param {number} x
 * @param {number} y
 * @param {number} z
 * @param {Partial<{
 *   mobHerdId: MobHerdId
 *   spawnerId: PlayerId
 *   mobDbId: MobDbId
 *   name: string
 *   playSoundOnSpawn: boolean
 *   variation: MobVariation<TMobType>
 *   physicsOptions: Partial<{
 *     width: number
 *     height: number
 *   }>
 * }>} [options]
 * @returns { MobId | null }
 *   - `null` if the mob could not be spawned.
 *     This can happen when there are too many mobs in the world
 *     for the current number of players in the lobby,
 *     or if the area is protected (e.g. by spawn area protection).
 */
attemptSpawnMob(mobType, x, y, z, options)
```

<a id="despawnmob"></a>

```js
/**
 * Dispose of a mob's state and remove them from the world without triggering "on death" flows.
 * Always succeeds.
 *
 * @param {MobId} mobId
 * @returns {void}
 */
despawnMob(mobId)
```

<a id="getdefaultmobsetting"></a>

```js
/**
 * Returns the current default value for a mob setting.
 *
 * @param {TMobType} mobType
 * @param {TMobSetting} setting
 * @returns {MobSettings<TMobType>[TMobSetting]}
 */
getDefaultMobSetting(mobType, setting)
```

<a id="setdefaultmobsetting"></a>

```js
/**
 * Set the default value for a mob setting.
 *
 * @param {TMobType} mobType
 * @param {TMobSetting} setting
 * @param {MobSettings<TMobType>[TMobSetting]} value
 * @returns {void}
 */
setDefaultMobSetting(mobType, setting, value)
```

<a id="getmobsetting"></a>

```js
/**
 * Get the current value of a mob setting for a specific mob.
 *
 * @param {MobId} mobId
 * @param {TMobSetting} setting
 * @param {boolean} [returnDefaultIfNotOverriden] - If true, return the default setting if not overridden.
 * @returns {MobSettings<MobType>[TMobSetting]}
 */
getMobSetting(mobId, setting, returnDefaultIfNotOverriden)
```

<a id="setmobsetting"></a>

```js
/**
 * Set the current value of a mob setting for a specific mob.
 *
 * @param {MobId} mobId
 * @param {TMobSetting} setting
 * @param {MobSettings<MobType>[TMobSetting]} value
 * @returns {void}
 */
setMobSetting(mobId, setting, value)
```

---

<div align="left">
  <h3>〔 <code><b>block functions</b></code> 〕</h3>
</div>

<a id="getblock"></a>

```js
/**
 * Get the name of a block.
 *
 * @param {number | [number, number, number]} x - Could be an array [x, y, z]. If so, the other params shouldn't be passed.
 * @param {number} [y]
 * @param {number} [z]
 * @returns {BlockName} - the name contained in blockMetadata.ts or "Air"
 */
getBlock(x, y, z)
```

<a id="getblockid"></a>

```js
/**
 * Used to get the block id at a specific position.
 * Intended only for use in hot code paths - default to getBlock for most use cases.
 *
 * @param {number} x
 * @param {number} y
 * @param {number} z
 * @returns {BlockId}
 */
getBlockId(x, y, z)
```

<a id="setblock"></a>

```js
/**
 * Set a block. Valid names are those either contained in blockMetadata.ts or are "Air"
 *
 * This function is optimised for setting broad swathes of blocks.
 * For example, if you have a 50x50x50 area you need to turn to air, it will run performantly if you call this in double nested loops.
 *
 * @param {number | [number, number, number]} x - Can be an array [x, y, z]
 * @param {number | BlockName} y - Should be the name if first param is array.
 * @param {number} [z]
 * @param {BlockName} [blockName]
 * @returns {void}
 */
setBlock(x, y, z, blockName)
```

<a id="attemptworldchangeblock"></a>

```js
/**
 * Initiate a block change "by the world".
 * This ends up calling the `onWorldChangeBlock()` callback and only makes the change if not prevented by game.
 * `initiatorDbId` is null if the change was initiated by the game code.
 *
 * @param { PlayerDbId | null } initiatorDbId
 * @param {number} x
 * @param {number} y
 * @param {number} z
 * @param {BlockName} blockName
 * @param {WorldBlockChangedInfo} [extraInfo]
 * @returns {"preventChange" | "preventDrop" | void}
 *   - "preventChange" if the change was prevented
 *   - "preventDrop" if the change was allowed but without dropping any items
 *   - `undefined` if the change was allowed with an item drop
 */
attemptWorldChangeBlock(initiatorDbId, x, y, z, blockName, extraInfo)
```

<a id="setblockrect"></a>

```js
/**
 * Helper function that sets all blocks in a rectangle to a specific block.
 *
 * @param {[number, number, number]} pos1 - array [x, y, z]
 * @param {[number, number, number]} pos2 - array [x, y, z]
 * @param {BlockName} blockName
 * @returns {void}
 */
setBlockRect(pos1, pos2, blockName)
```

<a id="setblockwalls"></a>

```js
/**
 * Create walls by providing two opposite corners of the cuboid.
 *
 * @param {[number, number, number]} pos1 - array [x, y, z]
 * @param {[number, number, number]} pos2 - array [x, y, z]
 * @param {BlockName} blockName
 * @param {boolean} [hasFloor]
 * @param {boolean} [hasCeiling]
 * @returns {void}
 */
setBlockWalls(pos1, pos2, blockName, hasFloor, hasCeiling)
```

<a id="setblockdata"></a>

```js
/**
 * Store data about a block in a performant manner. Data is cleared when block changes.
 *
 * @param {number} x
 * @param {number} y
 * @param {number} z
 * @param {object} data
 * @returns {void}
 */
setBlockData(x, y, z, data)
```

<a id="getblockdata"></a>

```js
/**
 * Get stored data about a block in a performant manner. Data is cleared when block changes.
 *
 * @param {number} x
 * @param {number} y
 * @param {number} z
 * @returns {any}
 */
getBlockData(x, y, z)
```

<a id="isblockinloadedchunk"></a>

```js
/**
 * Check if the block at a specific position is in a loaded chunk.
 *
 * @param {number} x
 * @param {number} y
 * @param {number} z
 * @returns {boolean}
 */
isBlockInLoadedChunk(x, y, z)
```

<a id="getblocksolidity"></a>

```js
/**
 * Returns whether a block is solid or not.
 * 
 * Example: grass block is solid, while ladder and water are not.
 * Will be true if the block is unloaded.
 *
 * @param {number | [number, number, number]} x - Could be an array [x, y, z]. If so, the other params shouldn't be passed.
 * @param {number} [y]
 * @param {number} [z]
 * @returns {boolean}
 */
getBlockSolidity(x, y, z)
```

<a id="getmetainfo"></a>

```js
/**
 * Splits the block name by '|'. If no meta info, metaInfo is "".
 *
 * @param {BlockName | null | undefined} blockName
 * @returns {ItemMetaInfo}
 */
getMetaInfo(blockName)
```

<a id="blocknametoblockid"></a>

```js
/**
 * Get the numeric id of a block used in the ndarrays returned from getChunk.
 * 
 * i.e. chunk.blockData.set(x, y, z, api.blockNameToBlockId("Dirt"))
 *   or chunk.blockData.get(x, y, z) === api.blockNameToBlockId("Dirt")
 *
 * @param {BlockName} blockName
 * @param {boolean} [allowInvalidBlock]
 *   - Don't throw an error if the block name is invalid.
 *   - Defaults false.
 *   - If true and name is invalid, returns null.
 * @returns { number | null }
 */
blockNameToBlockId(blockName, allowInvalidBlock)
```

<a id="blockidtoblockname"></a>

```js
/**
 * Goes from block id to block name.
 * The reverse of blockNameToBlockId.
 *
 * @param {BlockId} blockId
 * @returns {BlockName}
 */
blockIdToBlockName(blockId)
```

<a id="blockcoordtochunkid"></a>

```js
/**
 * Get the unique id of the chunk containing `position` in the current map.
 *
 * @param {[number, number, number]} position
 * @returns {string}
 */
blockCoordToChunkId(position)
```

<a id="chunkidtobotleftcoord"></a>

```js
/**
 * Get the coordinates of the block in the chunk with the lowest x, y, and z coordinates.
 *
 * @param {string} chunkId
 * @returns {[number, number, number]}
 */
chunkIdToBotLeftCoord(chunkId)
```

<a id="setcanchangeblock"></a>

```js
/**
 * Let a player change a block at a specific coordinate.
 * 
 * Useful when client option canChange is false.
 * Overrides blockRect and blockType settings, so also useful when you have disallowed changing of a block type with setCantChangeBlockType.
 * Using this on 1000s of blocks will cause lag - if that is needed, find a way to use setCanChangeBlockType.
 *
 * @param {PlayerId} playerId
 * @param {number} x
 * @param {number} y
 * @param {number} z
 * @returns {void}
 */
setCanChangeBlock(playerId, x, y, z)
```

<a id="setcantchangeblock"></a>

```js
/**
 * Prevents a player from changing a block at a specific coordinate.
 *
 * Useful when client option canChange is true.
 * Overrides blockRect and blockType settings, so also useful when you have allowed changing of a block type with setCantChangeBlockType.
 * Using this on 1000s of blocks will cause lag - if that is needed, find a way to use setCantChangeBlockType.
 *
 * @param {PlayerId} playerId
 * @param {number} x
 * @param {number} y
 * @param {number} z
 * @returns {void}
 */
setCantChangeBlock(playerId, x, y, z)
```

<a id="setcanchangeblocktype"></a>

```js
/**
 * Lets a player change a block type.
 *
 * Valid names are those contained within blockMetadata.ts and "Air"
 * Less priority than cant change block pos/can change block rect
 *
 * @param {PlayerId} playerId
 * @param {BlockName} blockName
 * @returns {void}
 */
setCanChangeBlockType(playerId, blockName)
```

<a id="setcantchangeblocktype"></a>

```js
/**
 * Stops a player from changeing a block type.
 *
 * Valid names are those contained within blockMetadata.ts and "Air"
 * Less priority than can change block pos/can change block rect
 *
 * @param {PlayerId} playerId
 * @param {BlockName} blockName
 * @returns {void}
 */
setCantChangeBlockType(playerId, blockName)
```

<a id="resetcanchangeblocktype"></a>

```js
/**
 * Remove any previous can/cant change block type settings for a player.
 *
 * @param {PlayerId} playerId
 * @param {BlockName} blockName
 * @returns {void}
 */
resetCanChangeBlockType(playerId, blockName)
```

<a id="setcanchangeblockrect"></a>

```js
/**
 * Make it so a player can change blocks within two points.
 *
 * Coordinates are inclusive. Example:
 * if [0, 0, 0] is pos1 and [1, 1, 1] is pos2,
 * then the 8 blocks contained within low and high will be able to be broken.
 * Overrides `setCantChangeBlockType()`
 *
 * @param {PlayerId} playerId
 * @param {[number, number, number]} pos1 - array [x, y, z]
 * @param {[number, number, number]} pos2 - array [x, y, z]
 * @returns {void}
 */
setCanChangeBlockRect(playerId, pos1, pos2)
```

<a id="setcantchangeblockrect"></a>

```js
/**
 * Make it so a player cant change blocks within two points.
 * 
 * Coordinates are inclusive. Example:
 * if [0, 0, 0] is pos1 and [1, 1, 1] is pos2,
 * then the 8 blocks contained within won't be able to be broken.
 * Overrides `setCanChangeBlockType()`
 *
 * @param {PlayerId} playerId
 * @param {[number, number, number]} pos1 - array [x, y, z]
 * @param {[number, number, number]} pos2 - array [x, y, z]
 * @returns {void}
 */
setCantChangeBlockRect(playerId, pos1, pos2)
```

<a id="resetcanchangeblockrect"></a>

```js
/**
 * Remove any previous can/cant change block rect settings for a player.
 *
 * @param {PlayerId} playerId
 * @param {[number, number, number]} pos1 - array [x, y, z]
 * @param {[number, number, number]} pos2 - array [x, y, z]
 * @returns {void}
 */
resetCanChangeBlockRect(playerId, pos1, pos2)
```

<a id="setwalkthroughtype"></a>

```js
/**
 * Allow a player to walk through a type of block.
 *
 * For blocks that are normally solid and not seethrough,
 * the player will experience slight visual glitches while inside the block.
 *
 * @param {PlayerId} playerId
 * @param {BlockName} blockName
 * @param {boolean} [disable]
 *   - If you have enabled a player to walk through a block and want to make the block solid for them again, pass this with true.
 *   - Otherwise you only need to pass playerId and blockName.
 * @returns {void}
 */
setWalkThroughType(playerId, blockName, disable)
```

<a id="setwalkthroughrect"></a>

```js
/**
 * Allow a player to walk through (or not walk through) voxels that are located within a given rectangle.
 * 
 * For blocks that are normally solid and not seethrough,
 * the player will experience slight visual glitches while inside the block.
 *
 * You could set both pos1 and pos2 to [0, 0, 0] to make only (0, 0, 0) walkthrough, for example.
 *
 * @param {PlayerId} playerId
 * @param {[number, number, number]} pos1 - The one corner of the cuboid. Array [x, y, z]
 * @param {[number, number, number]} pos2 - The top right corner of the cuboid. Array [x, y, z]
 * @param {WalkThroughType} updateType
 *   - The type of update. Whether to make a rect solid, or able to be walked through.
 *   - Pass `DEFAULT_WALK_THROUGH` with a previously passed rect to disable any walkthrough setting for that rect.
 * @returns {void}
 */
setWalkThroughRect(playerId, pos1, pos2, updateType)
```

<a id="raycastforblock"></a>

```js
/**
 * Raycast for a block in the world.
 * Given a position and a direction, find the first block that the "ray" hits.
 * Range radius limit is 6 voxels (blocks).
 *
 * @param {[number, number, number]} fromPos
 * @param {[number, number, number]} dirVec - unit direction vector
 * @returns {BlockRaycastResult}
 */
raycastForBlock(fromPos, dirVec)
```

<a id="playparticleeffect"></a>

```js
/**
 * Play particle effect on all clients, or only on some clients if `clientPredictedBy` is specified.
 *
 * @param {TempParticleSystemOptions} options
 * @param {PlayerId} [clientPredictedBy] - Play only on clients where client with playerId clientPredictedBy is not invisible, transparent, or themselves.
 * @returns {void}
 */
playParticleEffect(options, clientPredictedBy)
```

<a id="isinsiderect"></a>

```js
/**
 * Check if a position is within a cubic rectangle
 *
 * @param {[number, number, number]} coordsToCheck
 * @param {[number, number, number]} pos1 - position of one corner
 * @param {[number, number, number]} pos2 - position of opposite corner
 * @param {boolean} [addOneToMax]
 * @returns {boolean}
 */
isInsideRect(coordsToCheck, pos1, pos2, addOneToMax)
```

<a id="getchunk"></a>

```js
/**
 * NOTE: This method is currently NOT supporeted by Bloxd public scripting.
 * 
 * Only use this instead of getBlock if you REALLY need the performance (i.e. you are iterating over tens of thousands of blocks)
 * 
 * ReturnedObject.blockData is a 32x32x32 ndarray of block ids.
 * (see https://www.npmjs.com/package/ndarray)
 * Each block id is a 16-bit number.
 * The ndarray should only be read from, writing to it will result in desync between the server and client.
 *
 * @param {[number, number, number]} position - The returned chunk contains `position`
 * @returns {PNull<GameChunk>} - `null` if the chunk is not loaded in a persisted world. ReturnedObject.blockData is an ndarray that can be accessed.
 */
getChunk(position)
```

<a id="getemptychunk"></a>

```js
/**
 * Only use chunk helpers if you REALLY need the performance (i.e. you are iterating over tens of thousands of blocks)
 * 
 * ReturnedObject.blockData is a 32x32x32 ndarray of air.
 * (see https://www.npmjs.com/package/ndarray)
 * Each block id is a 16-bit number.
 *
 * @returns {GameChunk}
 */
getEmptyChunk()
```

---

<div align="left">
  <h3>〔 <code><b>items functions</b></code> 〕</h3>
</div>


<a id="giveitem"></a>

```js
/**
 * Give a player an item and a certain amount of that item.
 * Returns the amount of item added to the users inventory.
 *
 * @param {PlayerId} playerId
 * @param {string} itemName
 * @param {number} [itemAmount]
 * @param {ItemAttributes} [attributes]
 *   - An optional object for certain types of item.
 *   - For guns this can contain the `shotsLeft` field which is the amount of ammo the gun currently has.
 * @returns {number}
 */
giveItem(playerId, itemName, itemAmount, attributes)
```

<a id="removeitemname"></a>

```js
/**
 * Remove an amount of item from a player's inventory.
 *
 * @param {PlayerId} playerId
 * @param {string} itemName
 * @param {number} amount
 * @returns {void}
 */
removeItemName(playerId, itemName, amount)
```

<a id="setitemslot"></a>

```js
/**
 * Put an item in a specific index. Default hotbar is indexes 0-9.
 *
 * @param {PlayerId} playerId
 * @param {number} itemSlotIndex - 0-indexed
 * @param {string} itemName - Can be "Air", in which case itemAmount will be ignored and the slot will be cleared.
 * @param { number | null } [itemAmount] - `-1` for infinity. Should not be set, or `null`, for items that are not stackable.
 * @param {ItemAttributes} [attributes] - An optional object for certain types of item.
 * @param {boolean} [tellClient] - Whether to tell client about it - results in desync between client and server if client doesnt locally perform the same action.
 * @returns {void}
 */
setItemSlot(playerId, itemSlotIndex, itemName, itemAmount, attributes, tellClient)
```

<a id="getitemslot"></a>

```js
/**
 * Get the item at a specific index.
 *
 * @param {PlayerId} playerId
 * @param {number} itemSlotIndex
 * @returns { InvenItem | null }
 *   - `null` if there is no item at that index.
 *   - If there is an item, returns an object of the format { name: string, amount: PNull<number>, attributes: ItemAttributes }
 */
getItemSlot(playerId, itemSlotIndex)
```

<a id="gethelditem"></a>

```js
/**
 * Get the currently held item of a player.
 *
 * @param {PlayerId} playerId
 * @returns { InvenItem | null }
 *   - `null` if no item is being held.
 *   - If an item is held, return an object of the format { name: string, amount: PNull<number>, attributes: ItemAttributes }
 */
getHeldItem(playerId)
```

<a id="hasitem"></a>

```js
/**
 * Whether a player has an item.
 *
 * @param {PlayerId} playerId
 * @param {string} itemName
 * @returns {boolean}
 */
hasItem(playerId, itemName)
```

<a id="getinventoryitemamount"></a>

```js
/**
 * The amount of an itemName a player has.
 *
 * @param {PlayerId} playerId
 * @param {string} itemName
 * @returns {number}
 *   - `0` if the player has none.
 *   - negative number if infinite.
 */
getInventoryItemAmount(playerId, itemName)
```

<a id="setselectedinventorysloti"></a>

```js
/**
 * Force the player to have the i-th inventory slot selected.
 * 
 * Example: newI 0 makes the player have the 0th inventory slot selected.
 *
 * @param {PlayerId} playerId
 * @param {number} newI - integer from 0-9
 * @returns {void}
 */
setSelectedInventorySlotI(playerId, newI)
```

<a id="getselectedinventorysloti"></a>

```js
/**
 * Get a player's currently selected inventory slot.
 *
 * @param {PlayerId} playerId
 * @returns {number}
 */
getSelectedInventorySlotI(playerId)
```

<a id="getinventoryfreeslotcount"></a>

```js
/**
 * Get the amount of free slots in a player's inventory.
 *
 * @param {PlayerId} playerId
 * @returns {number}
 */
getInventoryFreeSlotCount(playerId)
```

<a id="inventoryisfull"></a>

```js
/**
 * Whether the player has space in their inventory to get new blocks.
 *
 * @param {PlayerId} playerId
 * @returns {boolean}
 */
inventoryIsFull(playerId)
```

<a id="clearinventory"></a>

```js
/**
 * Clear the players inventory.
 *
 * @param {PlayerId} playerId
 * @returns {void}
 */
clearInventory(playerId)
```

<a id="canopenstandardchest"></a>

```js
/**
 * Checks if a player is able to open a chest at a given location,
 * as per the rules laid out by the "onPlayerAttemptOpenChest" game callback.
 *
 * @param {PlayerId} playerId
 * @param {number} chestX
 * @param {number} chestY
 * @param {number} chestZ
 * @returns { boolean | null }
 *   - `true` if the player can open the chest.
 *   - `false` if they cannot.
 *   - `void` if the chest does not exist.
 */
canOpenStandardChest(playerId, chestX, chestY, chestZ)
```

<a id="givestandardchestitem"></a>

```js
/**
 * Give a standard chest an item and a certain amount of that item.
 *
 * @param {[number, number, number]} chestPos
 * @param {string} itemName
 * @param {number} [itemAmount]
 * @param {PlayerId} [playerId] - The player who is interacting with the chest.
 * @param {ItemAttributes} [attributes] - An optional object for certain types of item.
 * @returns {number} - The amount of item added to the chest.
 */
giveStandardChestItem(chestPos, itemName, itemAmount, playerId, attributes)
```

<a id="getstandardchestfreeslotcount"></a>

```js
/**
 * Get the amount of free slots in a standard chest.
 *
 * @param {number[]} chestPos
 * @returns { number | null } - `null` for non-chests.
 */
getStandardChestFreeSlotCount(chestPos)
```

<a id="getstandardchestitemamount"></a>

```js
/**
 * The amount of an itemName a standard chest has.
 *
 * @param {[number, number, number]} chestPos
 * @param {string} itemName
 * @returns {number}
 *   - `0` if the standard chest has none.
 *   - negative number if infinite.
 */
getStandardChestItemAmount(chestPos, itemName)
```

<a id="getstandardchestitemslot"></a>

```js
/**
 * Get the item at a chest slot.
 *
 * @param {[number, number, number]} chestPos
 * @param {number} slotIndex
 * @returns { InvenItem | null }
 *   - `null` if empty.
 *   - otherwise format { name: string, amount: PNull<number>, attributes: ItemAttributes }
 */
getStandardChestItemSlot(chestPos, slotIndex)
```

<a id="getstandardchestitems"></a>

```js
/**
 * Get all the items from a standard chest in order.
 * Use this instead of repetitive calls with `getStandardChestItemSlot()`.
 *
 * @param {[number, number, number]} chestPos
 * @returns {PNull<InvenItem>[]}
 */
getStandardChestItems(chestPos)
```

<a id="setstandardchestitemslot"></a>

```js
/**
 * @param {[number, number, number]} chestPos
 * @param {number} slotIndex - 0-indexed
 * @param {string} itemName - Can be "Air", in which case itemAmount will be ignored and the slot will be cleared.
 * @param {number} [itemAmount] - `-1` for infinity. Should not be set, or `null`, for items that are not stackable.
 * @param {PlayerId} [playerId] - The player who is interacting with the chest.
 * @param {ItemAttributes} [attributes] - An optional object for certain types of item.
 * @returns {void}
 */
setStandardChestItemSlot(chestPos, slotIndex, itemName, itemAmount, playerId, attributes)
```

<a id="getmoonstonechestitemslot"></a>

```js
/**
 * Get the item in a player's moonstone chest slot.
 *
 * @param {PlayerId} playerId
 * @param {number} idx
 * @returns { InvenItem | null } - `null` if empty.
 */
getMoonstoneChestItemSlot(playerId, idx)
```

<a id="getmoonstonechestitems"></a>

```js
/**
 * Get all the items from a moonstone chest in order.
 * Use this instead of repetitive calls with `getMoonstoneChestItemSlot()`.
 *
 * @param {PlayerId} playerId
 * @returns {PNull<InvenItem>[]}
 */
getMoonstoneChestItems(playerId)
```

<a id="setmoonstonechestitemslot"></a>

```js
/**
 * Moonstone chests are a type of chest where a player accesses the same contents no matter the location of the moonstone chest.
 *
 * @param {PlayerId} playerId
 * @param {number} slotIndex - 0-indexed
 * @param {string} itemName - Can be "Air", in which case itemAmount will be ignored and the slot will be cleared.
 * @param {number} [itemAmount] - `-1` for infinity. Should not be set, or `null`, for items that are not stackable.
 * @param {ItemAttributes} [metadata] - An optional object for certain types of item.
 * @returns {void}
 */
setMoonstoneChestItemSlot(playerId, slotIndex, itemName, itemAmount, metadata)
```

<a id="edititemcraftingrecipes"></a>

```js
/**
 * Edit the crafting recipes for a player.
 *
 * @param {PlayerId} playerId
 * @param {ItemName} itemName
 * @param {RecipesForItem} recipesForItem
 * @returns {void}
 */
editItemCraftingRecipes(playerId, itemName, recipesForItem)
```

<a id="resetitemcraftingrecipes"></a>

```js
/**
 * Reset the crafting recipes for a given back to its original bloxd state.
 *
 * @param {PlayerId} playerId
 * @param { string | null } itemName
 *   - resets all crafting recipes for the given player if `null`
 *   - otherwise resets the crafting recipes for the given item.
 * @returns {void}
 */
resetItemCraftingRecipes(playerId, itemName)
```

<a id="removeitemcraftingrecipes"></a>

```js
/**
 * Removes crafting recipes.
 *
 * @param {PlayerId} playerId
 * @param { string | null } itemName
 *   - removes all crafting recipes for the given player if `null`,
 *   - otherwise removes the crafting recipes for the given item.
 * @returns {void}
 */
removeItemCraftingRecipes(playerId, itemName)
```

<a id="createitemdrop"></a>

```js
/**
 * Create a dropped item.
 *
 * @param {number} x
 * @param {number} y
 * @param {number} z
 * @param {string} itemName - Name of the item. Valid names can be found in blockMetadata.ts and itemMetadata.ts
 * @param { number | null } [amount] - The amount of the item to include in the drop - so when the player picks up the item drop, they get this many of the item.
 * @param {boolean} [mergeItems] - Whether to merge the item into an nearby item of same type, if one exists. Defaults to false.
 * @param {ItemAttributes} [attributes] - Attributes of the item being dropped
 * @param {number} [timeTillDespawn] - Time till the item automatically despawns in milliseconds. Max of 5 minutes (300_000 ms).
 * @returns { EntityId | null } - The id you can pass to setCantPickUpItem, or null if the item drop limit was reached.
 */
createItemDrop(x, y, z, itemName, amount, mergeItems, attributes, timeTillDespawn)
```

<a id="setitemamount"></a>

```js
/**
 * Set the amount of an item in an item entity.
 *
 * @param {EntityId} itemId
 * @param {number} newAmount
 * @returns {void}
 */
setItemAmount(itemId, newAmount)
```

<a id="deleteitemdrop"></a>

```js
/**
 * Delete an item drop by entity id.
 *
 * @param {EntityId} itemId
 * @returns {void}
 */
deleteItemDrop(itemId)
```

<a id="setcantpickupitem"></a>

```js
/**
 * Prevent a player from picking up an item.
 * `itemId` returned by `createItemDrop()` can be used.
 *
 * @param {PlayerId} playerId
 * @param {EntityId} itemId
 * @returns {void}
 */
setCantPickUpItem(playerId, itemId)
```

<a id="getinitialitemmetadata"></a>

```js
/**
 * Get the metadata about a block or item before stats have been modified by any client options.
 * (i.e. its entry in either blockMetadata.ts or nonBlockMetadata in itemMetadata.ts)
 *
 * @param {string} itemName
 * @returns {Partial<BlockMetadataItem & NonBlockMetadataItem>}
 */
getInitialItemMetadata(itemName)
```

<a id="getitemstat"></a>

```js
/**
 * Get stat info about a block or item.
 * 
 * Either based on a client option for a player: (e.g. `DirtTtb`)
 * or its entry in blockMetadata.ts or nonBlockMetadata in itemMetadata.ts if no client option is set.
 *
 * If null is passed for lifeformId, this is simply its entry in blockMetadata etc.
 *
 * @param { LifeformId | null } lifeformId
 * @param {string} itemName
 * @param {K} stat
 * @returns {AnyMetadataItem[K]}
 */
getItemStat(lifeformId, itemName, stat)
```

---

<div align="left">
  <h3>〔 <code><b>lobby functions</b></code> 〕</h3>
</div>

<a id="now"></a>

```js
/**
 * Obtain cached Date.now() value saved at the end of previous game tick.
 *
 * @returns {number}
 */
now()
```

<a id="getlobbyname"></a>

```js
/**
 * Get the name of the lobby this game is running in.
 *
 * @returns { string | null }
 */
getLobbyName()
```

<a id="ispubliclobby"></a>

```js
/**
 * Integer lobby names are public.
 *
 * @returns {boolean} - boolean
 */
isPublicLobby()
```

<a id="getlobbytype"></a>

```js
/**
 * Returns if the current lobby the game is running in is special - e.g. a discord guild or simply a standard lobby.
 *
 * @returns {LobbyType}
 */
getLobbyType()
```

<a id="setmaxplayers"></a>

```js
/**
 * Update the max players and soft max players the matchmaking will use.
 *
 * `softMaxPlayers` is the number of players that matchmaking will route to using "Quick Play".
 * Once the softMaxPlayers limit is reached, this lobby can only be joined by requesting the lobby name or joining a friend.
 *
 * `maxPlayers` is the absolute maximum: a lobby will not have more players than this.
 * TIP: softMaxPlayers should be around 90% of maxPlayers
 *
 * WARNING: This change is not immediate, as it takes a while for matchmaking to find out.
 * Also, this will not kick players out of the lobby if set to a lower value than the current player count.
 *
 * @param {number} softMaxPlayers
 * @param {number} maxPlayers
 * @returns {void}
 */
setMaxPlayers(softMaxPlayers, maxPlayers)
```

---

<div align="left">
  <h3>〔 <code><b>callback functions</b></code> 〕</h3>
</div>

<a id="setcallbackvaluefallback"></a>

```js
/**
 * Set a default value to be returned by your callback code if it throws any type of error.
 *
 * @param {string} callbackName
 * @param {any} defaultValue
 */
api.setCallbackValueFallback(callbackName, defaultValue)
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
type ItemAttributes = { customDisplayName?: string; customDescription?: string; customAttributes?: Record<string, any> }
```

```ts
type RecipesForItem =
  {
    requires: { items: ItemName[]; amt: number }[]
    produces: number
    station?: string | string[]
    onCraftedAura?: number
    isStarterRecipe?: boolean
  }[]
```

```ts
enum WalkThroughType {
  CANT_WALK_THROUGH = 0,
  CAN_WALK_THROUGH = 1,
  DEFAULT_WALK_THROUGH = 2,
}
```

```ts
enum ExplosionType {
  BOOM = 0,
  FREEZE = 1,
  BUBBLE = 2,
}
```

```ts
type WorldBlockChangedInfo = {
  cause: PNull<"Paintball" | "FloorCreator" | "Sapling" | "StemFruit" | "MeltingIce" | "Explosion">
}
```

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
type StyledIcon = {
  icon: string
  style?: {
    color?: string
    colour?: string
    fontSize?: string
    opacity?: number
  }
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

