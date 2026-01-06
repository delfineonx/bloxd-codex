
---

<div align="center">
  <h1>MOB SETTINGS</h1>
  <p>
    <a href="#api-methods"><kbd>API Methods</kbd></a> &nbsp;•&nbsp; 
    <a href="#settings"><kbd>Settings</kbd></a> &nbsp;•&nbsp; 
    <a href="#types-and-variations"><kbd>Types &amp; Variations</kbd></a> &nbsp;•&nbsp; 
    <a href="#usage"><kbd>Usage</kbd></a>
  </p>
</div>

---

<a id="api-methods"></a>

<div align="center">
	<h2>❮ <code><b>API Methods</b></code> ❯</h2> 
</div>

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

<a id="settings"></a>

<div align="center">
	<h2>❮ <code><b>Settings</b></code> ❯</h2> 
</div>

<div align="center">
  <table>
    <tr>
      <td valign="top" align="left"><h4>
        <a href="#variation"><code>variation</code></a><br>
        <a href="#name"><code>name</code></a><br>
        <a href="#maxhealth"><code>maxHealth</code></a><br>
        <a href="#initialhealth"><code>initialHealth</code></a><br>
        <a href="#idlesound"><code>idleSound</code></a><br>
        <a href="#attacksound"><code>attackSound</code></a><br>
        <a href="#secondaryattacksound"><code>secondaryAttackSound</code></a><br>
        <a href="#hurtsound"><code>hurtSound</code></a><br>
        <a href="#ondeathitemdrops"><code>onDeathItemDrops</code></a><br>
        <a href="#ondeathparticletexture"><code>onDeathParticleTexture</code></a><br>
        <a href="#ondeathaura"><code>onDeathAura</code></a><br>
        <a href="#basewalkingspeed"><code>baseWalkingSpeed</code></a><br>
        <a href="#baserunningspeed"><code>baseRunningSpeed</code></a><br>
        <a href="#walkingspeedmultiplier"><code>walkingSpeedMultiplier</code></a><br>
        <a href="#runningspeedmultiplier"><code>runningSpeedMultiplier</code></a><br>
        <a href="#jumpcount"><code>jumpCount</code></a><br>
      </h4></td>
      <td valign="top" align="left"><h4>
        <a href="#basejumpimpulsexz"><code>baseJumpImpulseXZ</code></a><br>
        <a href="#basejumpimpulsey"><code>baseJumpImpulseY</code></a><br>
        <a href="#jumpmultiplier"><code>jumpMultiplier</code></a><br>
        <a href="#runawayradius"><code>runAwayRadius</code></a><br>
        <a href="#chaseradius"><code>chaseRadius</code></a><br>
        <a href="#territoryradius"><code>territoryRadius</code></a><br>
        <a href="#hostilityradius"><code>hostilityRadius</code></a><br>
        <a href="#stoppingradius"><code>stoppingRadius</code></a><br>
        <a href="#attackinterval"><code>attackInterval</code></a><br>
        <a href="#attackradius"><code>attackRadius</code></a><br>
        <a href="#secondaryattackradius"><code>secondaryAttackRadius</code></a><br>
        <a href="#attackdamage"><code>attackDamage</code></a><br>
        <a href="#secondaryattackdamage"><code>secondaryAttackDamage</code></a><br>
        <a href="#attackimpulse"><code>attackImpulse</code></a><br>
        <a href="#secondaryattackimpulse"><code>secondaryAttackImpulse</code></a><br>
      </h4></td>
      <td valign="top" align="left"><h4>
        <a href="#helditemname"><code>heldItemName</code></a><br>
        <a href="#attackitemname"><code>attackItemName</code></a><br>
        <a href="#secondaryattackitemname"><code>secondaryAttackItemName</code></a><br>
        <a href="#attackeffectname"><code>attackEffectName</code></a><br>
        <a href="#attackeffectduration"><code>attackEffectDuration</code></a><br>
        <a href="#tameinfo"><code>tameInfo</code></a><br>
        <a href="#ontamedhealthmultiplier"><code>onTamedHealthMultiplier</code></a><br>
        <a href="#ownerdbid"><code>ownerDbId</code></a><br>
        <a href="#minfollowingradius"><code>minFollowingRadius</code></a><br>
        <a href="#maxfollowingradius"><code>maxFollowingRadius</code></a><br>
        <a href="#isrideable"><code>isRideable</code></a><br>
        <a href="#healthregen"><code>healthRegen</code></a><br>
        <a href="#ridingspeedmult"><code>ridingSpeedMult</code></a><br>
        <a href="#metainfo"><code>metaInfo</code></a><br>
        <a href="#petinfo"><code>petInfo</code></a><br>
      </h4></td>
    </tr>
  </table>
</div>

---

<a id="variation"></a>

```js
/**
 * @type {"default"}
 */
variation = "default"
```

---

<a id="name"></a>

```js
/**
 * @type {string}
 */
name = ""
```

---

<a id="maxhealth"></a>

```js
/**
 * @type {number}
 */
maxHealth = 75
```

---

<a id="initialhealth"></a>

```js
/**
 * @type {number}
 */
initialHealth = 75
```

---

<a id="idlesound"></a>

```js
/**
 * @type {string}
 */
idleSound = "pigOink"
```

---

<a id="attacksound"></a>

```js
/**
 * @type {string}
 */
attackSound = null
```

---

<a id="secondaryattacksound"></a>

```js
/**
 * @type {string}
 */
secondaryAttackSound = null
```

---

<a id="hurtsound"></a>

```js
/**
 * @type {string}
 */
hurtSound = "pigHurt"
```

---

<a id="ondeathitemdrops"></a>

```js
/**
 * @type { { itemName: string; probabilityOfDrop: number; dropMinAmount: number; dropMaxAmount: number; applyBurstImpulseToDrop?: boolean; }[] }
 */
onDeathItemDrops = [
    {
        itemName: "Raw Porkchop",
        probabilityOfDrop: 1,
        dropMinAmount: 1,
        dropMaxAmount: 3,
    },
]
```

---

<a id="ondeathparticletexture"></a>

```js
/**
 * @type {string}
 */
onDeathParticleTexture = "critical_hit"
```

---

<a id="ondeathaura"></a>

```js
/**
 * @type {number}
 */
onDeathAura = 20
```

---

<a id="basewalkingspeed"></a>

```js
/**
 * @type {number}
 */
baseWalkingSpeed = 3.5
```

---

<a id="baserunningspeed"></a>

```js
/**
 * @type {number}
 */
baseRunningSpeed = 4.55 * 0.85
```

---

<a id="walkingspeedmultiplier"></a>

```js
/**
 * @type {number}
 */
walkingSpeedMultiplier = 1
```

---

<a id="runningspeedmultiplier"></a>

```js
/**
 * @type {number}
 */
runningSpeedMultiplier = 1
```

---

<a id="jumpcount"></a>

```js
/**
 * @type {number}
 */
jumpCount = 0
```

---

<a id="basejumpimpulsexz"></a>

```js
/**
 * @type {number}
 */
baseJumpImpulseXZ = 0
```

---

<a id="basejumpimpulsey"></a>

```js
/**
 * @type {number}
 */
baseJumpImpulseY = 0
```

---

<a id="jumpmultiplier"></a>

```js
/**
 * @type {number}
 */
jumpMultiplier = 1
```

---

<a id="runawayradius"></a>

```js
/**
 * @type {number}
 */
runAwayRadius = 0
```

---

<a id="chaseradius"></a>

```js
/**
 * @type {number}
 */
chaseRadius = 0
```

---

<a id="territoryradius"></a>

```js
/**
 * @type {number}
 */
territoryRadius = 0
```

---

<a id="hostilityradius"></a>

```js
/**
 * @type {number}
 */
hostilityRadius = 0
```

---

<a id="stoppingradius"></a>

```js
/**
 * @type {number}
 */
stoppingRadius = 0.5
```

---

<a id="attackinterval"></a>

```js
/**
 * @type {number}
 */
attackInterval = 0
```

---

<a id="attackradius"></a>

```js
/**
 * @type {number}
 */
attackRadius = 0
```

---

<a id="secondaryattackradius"></a>

```js
/**
 * @type {number}
 */
secondaryAttackRadius = 0
```

---

<a id="attackdamage"></a>

```js
/**
 * @type {number}
 */
attackDamage = 0
```

---

<a id="secondaryattackdamage"></a>

```js
/**
 * @type {number}
 */
secondaryAttackDamage = 0
```

---

<a id="attackimpulse"></a>

```js
/**
 * @type {number}
 */
attackImpulse = 0
```

---

<a id="secondaryattackimpulse"></a>

```js
/**
 * @type {number}
 */
secondaryAttackImpulse = 0
```

---

<a id="helditemname"></a>

```js
/**
 * @type {string}
 */
heldItemName = null
```

---

<a id="attackitemname"></a>

```js
/**
 * @type {string}
 */
attackItemName = null
```

---

<a id="secondaryattackitemname"></a>

```js
/**
 * @type {string}
 */
secondaryAttackItemName = null
```

---

<a id="attackeffectname"></a>

```js
/**
 * @type {string}
 */
attackEffectName = null
```

---

<a id="attackeffectduration"></a>

```js
/**
 * @type {number}
 */
attackEffectDuration = 0
```

---

<a id="tameinfo"></a>

```js
/**
 * @type {MobTameInfo}
 */
tameInfo = {
    tameItemName: [
        "Raw Porkchop",
        "Raw Beef",
        "Raw Mutton",
        "Raw Venison",
        "Cooked Porkchop",
        "Steak",
        "Cooked Mutton",
        "Cooked Venison"
    ],
    probabilityOfTame: 0.32,
    isSaddleable: false,
    supportsFriendship: true,
    likedFoods: [
        "Raw Porkchop",
        "Raw Beef",
        "Raw Mutton",
        "Raw Venison",
        "Cooked Porkchop",
        "Steak",
        "Cooked Mutton",
        "Cooked Venison",
        "Banana",
        "Baked Potato",
        "Rotten Brain"
    ],
    neutralFoods: [
        "Catnip",
        "Pumpkin Pie",
        "Bowl of Cranberries",
        "Watermelon Slice",
        "Gold Watermelon Slice",
        "Bread",
        "Rotten Flesh",
        "Mushroom Soup",
        "Plum",
        "Carrot",
        "Beetroot",
        "Raw Potato"
    ],
    dislikedFoods: [
        "Apple",
        "Wheat",
        "Pear",
        "Cherry",
        "Bowl of Rice",
        "Melon Slice",
        "Gold Melon Slice",
        "Chili Pepper",
        "Cracked Coconut"
    ],
    foodItemsWithEffects: [
        {
            itemName: "Catnip",
            effects: [
                {
                    name: "Speed",
                    duration: 30000,
                    level: 1
                },
                {
                    name: "Damage",
                    duration: 30000,
                    level: 1
                }
            ]
        }
    ],
    guaranteedDrop: "Caught Fish",
    commonDrops: [
        "Poop",
        "Wheat Seeds"
    ],
    levelUpBonuses: {
        1: "Renaming",
        2: "Special Drops",
        3: "Damage +",
        4: "Painting",
        5: "Poison Claws"
    }
}
```

---

<a id="ontamedhealthmultiplier"></a>

```js
/**
 * @type {number}
 */
onTamedHealthMultiplier = 4.0
```

---

<a id="ownerdbid"></a>

```js
/**
 * @type {string}
 */
ownerDbId = null
```

---

<a id="minfollowingradius"></a>

```js
/**
 * @type {number}
 */
minFollowingRadius = 5
```

---

<a id="maxfollowingradius"></a>

```js
/**
 * @type {number}
 */
maxFollowingRadius = 12
```

---

<a id="isrideable"></a>

```js
/**
 * @type {boolean}
 */
isRideable = false
```

---

<a id="healthregen"></a>

```js
/**
 * @type { { amount: number; interval: number; startAfter: number; } }
 */
healthRegen = null
```

---

<a id="ridingspeedmult"></a>

```js
/**
 * @type {number}
 */
ridingSpeedMult = 1
```

---

<a id="metainfo"></a>

```js
/**
 * @type {string}
 */
metaInfo = ""
```

---

<a id="petinfo"></a>

```js
/**
 * @type {MobPetInfo}
 */
petInfo = {
    friendshipPoints: 0,
    lastFedAt: null,
    highestFriendshipLevelReached: 0,
    superlikedFood: null,
    superlikedFoodKnown: false,
    bonusesGained: [],
}
```

---

<a id="types-and-variations"></a>

<div align="center">
	<h2>❮ <code><b>Types & Variations</b></code> ❯</h2> 
</div>

```json
{
  "Pig": ["default"],
  "Cow": ["default", "cream"],
  "Sheep": [
    "default",
    "black",
    "red",
    "orange",
    "pink",
    "purple",
    "yellow",
    "blue",
    "brown",
    "cyan",
    "gray",
    "green",
    "lightBlue",
    "lightGray",
    "lime",
    "magenta"
  ],
  "Horse": ["default", "black", "brown", "cream"],
  "Cave Golem": ["default", "iron"],
  "Draugr Zombie": ["default", "longHairChestplate", "longHairClothed", "shortHairClothed"],
  "Draugr Skeleton": ["default"],
  "Frost Golem": ["default"],
  "Frost Zombie": ["default", "longHairChestplate", "shortHairClothed"],
  "Frost Skeleton": ["default"],
  "Draugr Knight": ["default"],
  "Wolf": ["default", "white", "brown", "grey", "spectral"],
  "Bear": ["default"],
  "Deer": ["default"],
  "Stag": ["default"],
  "Gold Watermelon Stag": ["default"],
  "Gorilla": ["default"],
  "Wildcat": [
    "default",
    "tabby",
    "grey",
    "black",
    "calico",
    "siamese",
    "leopard"
  ],
  "Magma Golem": ["default"],
  "Draugr Huntress": ["default", "chainmail"],
  "Spirit Golem": ["default"],
  "Spirit Wolf": ["default"],
  "Spirit Bear": ["default"],
  "Spirit Stag": ["default"],
  "Spirit Gorilla": ["default"]
}
```

<a id="usage"></a>

<div align="center">
	<h2>❮ <code><b>Usage</b></code> ❯</h2> 
</div>

```js
// Quick helper to get all current values of mob settings for a specific mob.

const mobSettingNames = [
  "variation",
  "name",
  "maxHealth",
  "initialHealth",
  "idleSound",
  "attackSound",
  "secondaryAttackSound",
  "hurtSound",
  "onDeathItemDrops",
  "onDeathParticleTexture",
  "onDeathAura",
  "baseWalkingSpeed",
  "baseRunningSpeed",
  "walkingSpeedMultiplier",
  "runningSpeedMultiplier",
  "jumpCount",
  "baseJumpImpulseXZ",
  "baseJumpImpulseY",
  "jumpMultiplier",
  "runAwayRadius",
  "chaseRadius",
  "territoryRadius",
  "hostilityRadius",
  "stoppingRadius",
  "attackInterval",
  "attackRadius",
  "secondaryAttackRadius",
  "attackDamage",
  "secondaryAttackDamage",
  "attackImpulse",
  "secondaryAttackImpulse",
  "heldItemName",
  "attackItemName",
  "secondaryAttackItemName",
  "attackEffectName",
  "attackEffectDuration",
  "tameInfo",
  "onTamedHealthMultiplier",
  "ownerDbId",
  "minFollowingRadius",
  "maxFollowingRadius",
  "isRideable",
  "healthRegen",
  "ridingSpeedMult",
  "metaInfo",
  "petInfo",
];

getMobFullSettings = (mobId) => {
  if (!api.checkValid(mobId)) {
    return null;
  }
  const out = {};
  let name;
  for (let i = 0, n = mobSettingNames.length; i < n; i++) {
    name = mobSettingNames[i];
    out[name] = api.getMobSetting(mobId, name);
  }
  return out;
};
```

---
