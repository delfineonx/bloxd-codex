---

<div align="center">
  <h1>ENCHANTING</h1>
  <p>
    <a href="#api-methods"><kbd>API Methods</kbd></a>
    &nbsp;•&nbsp; <a href="#usage"><kbd>Usage</kbd></a>
    &nbsp;•&nbsp; <a href="#names"><kbd>Names</kbd></a>
    &nbsp;•&nbsp; <a href="#probabilities"><kbd>Probabilities</kbd></a>
  </p>
</div>

---

<a id="api-methods"></a>

<div align="center">
  <h2>❮ <code><b>API Methods</b></code> ❯</h2>
</div>

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

```js
/**
 * Put an item in a specific index. Default hotbar is indexes 0-9.
 *
 * @param {PlayerId} playerId
 * @param {number} itemSlotIndex - 0-indexed
 * @param {string} itemName - Can be "Air", in which case itemAmount will be ignored and the slot will be cleared.
 * @param {PNull<number>} [itemAmount] - `-1` for infinity. Should not be set, or `null`, for items that are not stackable.
 * @param {ItemAttributes} [attributes] - An optional object for certain types of item.
 * @param {boolean} [tellClient] - Whether to tell client about it - results in desync between client and server if client doesnt locally perform the same action.
 * @returns {void}
 */
setItemSlot(playerId, itemSlotIndex, itemName, itemAmount, attributes, tellClient)
```

---

<a id="usage"></a>

<div align="center">
  <h2>❮ <code><b>Usage</b></code> ❯</h2>
</div>

```js
api.giveItem(playerId, "Diamond Sword", null, {
  // customDisplayName: "someName",
  // customDescription: "someDesc",
  customAttributes: {
    enchantments: {
      "Critical Damage": 2,
      "Damage": 5,
      "Vertical Knockback": 3,
      // ...
    },
    // enchantmentTier: "Tier 4"
  }
});
```

---

<a id="names"></a>

<div align="center">
  <h2>❮ <code><b>Names</b></code> ❯</h2>
</div>

<div align="center">
  <h4>
    ✦ <code><b>Credits</b></code> ✦<br>
    <b>Thanks to <code>the_ccccc</code> for creating and posting these!</b>
  </h4> 
</div>

```js
enchantments_list = [
  "Protection",
  "Health",
  "Health Regen",
  "Damage",
  "Critical Damage",
  "Attack Speed",
  "Momentum",
  "Break Speed",
  "Yield",
  "Aura",
  "Stomp",
  "Protection",
  "Knockback",
  "Arrow Speed",
  "Arrow Damage",
  "Quick Charge'" 
  "Knockback Resist'" 
  "Horizontal Knockback",
  "Vertical Knockback",
];
```

```js
items_enchantments = {
  "armor": ["Protection", "Health", "Health Regen"],
  "sword": ["Damage", "Critical Damage", "Attack Speed"],
  "pickaxe": ["Momentum", "Break speed", "Yield", "Aura"],
  "hoe": ["Momentum", "Break Speed", "Yield", "Aura"],
  "axe": ["Momentum", "Break Speed", "Aura"],
  "spade": ["Momentum", "Break Speed", "Aura"],
  "fur boots": ["Stomp", "Protection", "Health", "Health Regen"],
  "knight sword": ["Damage", "Critical Damage", "Attack Speed", "Knockback"],
  "moonstone pickaxe": ["Momentum", "Break Speed", "Aura"],
  "bow": ["Arrow Speed", "Arrow Damage", "Quick Charge"],
  "fur chestplate": ["Knockback Resist", "Protection", "Health", "Health Regen"],
  "stick": ["Horizontal Knockback", "Vertical Knockback", "Damage"],
};
```

---

<a id="probabilities"></a>

<div align="center">
  <h2>❮ <code><b>Probabilities</b></code> ❯</h2>
</div>

```js
level_probs_by_input = {
  80: [(5, 0.2057), (4, 0.7943)],
  79: [(5, 0.1991), (4, 0.8009)],
  78: [(5, 0.1927), (4, 0.8073)],
  77: [(5, 0.1867), (4, 0.8133)],
  76: [(5, 0.1809), (4, 0.8191)],
  75: [(5, 0.1753), (4, 0.8247)],
  74: [(5, 0.1699), (4, 0.8301)],
  73: [(5, 0.1546), (4, 0.7833), (3, 0.0621)],
  72: [(5, 0.1478), (4, 0.7767), (3, 0.0755)],
  71: [(5, 0.1412), (4, 0.7688), (3, 0.0900)],
  70: [(5, 0.1346), (4, 0.7598), (3, 0.1056)],
  69: [(5, 0.1283), (4, 0.7496), (3, 0.1221)],
  68: [(5, 0.1220), (4, 0.7383), (3, 0.1397)],
  67: [(5, 0.1160), (4, 0.7259), (3, 0.1581)],
  66: [(5, 0.1100), (4, 0.7127), (3, 0.1773)],
  65: [(5, 0.1043), (4, 0.6985), (3, 0.1972)],
  64: [(5, 0.0987), (4, 0.6835), (3, 0.2178)],
  63: [(5, 0.0933), (4, 0.6678), (3, 0.2389)],
  62: [(5, 0.0880), (4, 0.6514), (3, 0.2606)],
  61: [(5, 0.0830), (4, 0.6343), (3, 0.2827)],
  60: [(5, 0.0781), (4, 0.6167), (3, 0.3052)],
  59: [(5, 0.0734), (4, 0.5987), (3, 0.3279)],
  58: [(5, 0.0689), (4, 0.5802), (3, 0.3509)],
  57: [(5, 0.0645), (4, 0.5615), (3, 0.3740)],
  56: [(5, 0.0603), (4, 0.5424), (3, 0.3973)],
  55: [(5, 0.0564), (4, 0.5237), (3, 0.4199)],
  54: [(5, 0.0525), (4, 0.5039), (3, 0.4436)],
  53: [(5, 0.0489), (4, 0.4845), (3, 0.4666)],
  52: [(5, 0.0466), (4, 0.4769), (3, 0.4765)],
  51: [(5, 0.0439), (4, 0.4638), (3, 0.4923)],
  50: [(5, 0.0390), (4, 0.4266), (3, 0.4785), (2, 0.0559)],
  49: [(5, 0.0361), (4, 0.4075), (3, 0.4812), (2, 0.0752)],
  48: [(5, 0.0333), (4, 0.3887), (3, 0.4813), (2, 0.0967)],
  47: [(5, 0.0307), (4, 0.3701), (3, 0.4792), (2, 0.1200)],
  46: [(5, 0.0282), (4, 0.3519), (3, 0.4749), (2, 0.1450)],
  45: [(5, 0.0259), (4, 0.3340), (3, 0.4687), (2, 0.1714)],
  44: [(5, 0.0237), (4, 0.3164), (3, 0.4610), (2, 0.1989)],
  43: [(5, 0.0216), (4, 0.2993), (3, 0.4517), (2, 0.2274)],
  42: [(5, 0.0197), (4, 0.2826), (3, 0.4411), (2, 0.2566)],
  41: [(5, 0.0180), (4, 0.2665), (3, 0.4291), (2, 0.2864)],
  40: [(5, 0.0163), (4, 0.2508), (3, 0.4164), (2, 0.3165)],
  39: [(5, 0.0148), (4, 0.2356), (3, 0.4028), (2, 0.3468)],
  38: [(5, 0.0134), (4, 0.2209), (3, 0.3886), (2, 0.3771)],
  37: [(5, 0.0120), (4, 0.2068), (3, 0.3739), (2, 0.4073)],
  36: [(5, 0.0108), (4, 0.1933), (3, 0.3586), (2, 0.4373)],
  35: [(5, 0.0097), (4, 0.1803), (3, 0.3431), (2, 0.4669)],
  34: [(5, 0.0087), (4, 0.1678), (3, 0.3275), (2, 0.4960)],
  33: [(5, 0.0078), (4, 0.1560), (3, 0.3117), (2, 0.5245)],
  32: [(5, 0.0069), (4, 0.1447), (3, 0.2960), (2, 0.5524)],
  31: [(5, 0.0061), (4, 0.1341), (3, 0.2807), (2, 0.5791)],
  30: [(5, 0.0055), (4, 0.1246), (3, 0.2668), (2, 0.6031)],
  29: [(5, 0.0049), (4, 0.1162), (3, 0.2543), (2, 0.6246)],
  28: [(5, 0.0044), (4, 0.1086), (3, 0.2429), (2, 0.6441)],
  27: [(5, 0.0037), (4, 0.0965), (3, 0.2205), (2, 0.6278), (1, 0.0515)],
  26: [(5, 0.0032), (4, 0.0884), (3, 0.2064), (2, 0.6284), (1, 0.0736)],
  25: [(5, 0.0028), (4, 0.0809), (3, 0.1928), (2, 0.6251), (1, 0.0984)],
  24: [(5, 0.0025), (4, 0.0738), (3, 0.1797), (2, 0.6185), (1, 0.1255)],
  23: [(5, 0.0021), (4, 0.0672), (3, 0.1670), (2, 0.6091), (1, 0.1546)],
  22: [(5, 0.0018), (4, 0.0611), (3, 0.1549), (2, 0.5971), (1, 0.1851)],
  21: [(5, 0.0016), (4, 0.0554), (3, 0.1434), (2, 0.5827), (1, 0.2169)],
  20: [(5, 0.0013), (4, 0.0501), (3, 0.1324), (2, 0.5667), (1, 0.2495)],
  19: [(5, 0.0012), (4, 0.0452), (3, 0.1219), (2, 0.5490), (1, 0.2827)],
  18: [(5, 0.0010), (4, 0.0407), (3, 0.1120), (2, 0.5301), (1, 0.3162)],
  17: [(5, 0.0008), (4, 0.0365), (3, 0.1027), (2, 0.5102), (1, 0.3498)],
  16: [(5, 0.0007), (4, 0.0327), (3, 0.0939), (2, 0.4894), (1, 0.3833)],
  15: [(5, 0.0006), (4, 0.0292), (3, 0.0857), (2, 0.4681), (1, 0.4164)],
  14: [(5, 0.0005), (4, 0.0261), (3, 0.0780), (2, 0.4464), (1, 0.4490)],
  13: [(5, 0.0004), (4, 0.0232), (3, 0.0708), (2, 0.4246), (1, 0.4810)],
  12: [(5, 0.0003), (4, 0.0205), (3, 0.0641), (2, 0.4028), (1, 0.5123)],
  11: [(5, 0.0003), (4, 0.0181), (3, 0.0579), (2, 0.3811), (1, 0.5426)],
  10: [(5, 0.0002), (4, 0.0160), (3, 0.0521), (2, 0.3596), (1, 0.5721)],
  9: [(5, 0.0002), (4, 0.0141), (3, 0.0468), (2, 0.3385), (1, 0.6004)],
  8: [(5, 0.0001), (4, 0.0123), (3, 0.0420), (2, 0.3178), (1, 0.6278)],
  7: [(5, 0.0001), (4, 0.0108), (3, 0.0375), (2, 0.2977), (1, 0.6539)],
  6: [(5, 0.00009), (4, 0.0094), (3, 0.0334), (2, 0.2782), (1, 0.67891)],
  5: [(5, 0.00007), (4, 0.0081), (3, 0.0297), (2, 0.2594), (1, 0.70273)],
  4: [(5, 0.00006), (4, 0.0070), (3, 0.0263), (2, 0.24127), (1, 0.72537)],
  3: [(5, 0.00004), (4, 0.0060), (3, 0.0232), (2, 0.22393), (1, 0.74683)],
  2: [(5, 0.00003), (4, 0.0052), (3, 0.0205), (2, 0.2073), (1, 0.76697)],
  1: [(5, 0.00003), (4, 0.0044), (3, 0.0180), (2, 0.1915), (1, 0.78607)],
}
```

---

