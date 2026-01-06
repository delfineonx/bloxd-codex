
---

<div align="center">
  <h1>SOUNDS</h1>
  <p>
    <a href="#api-methods"><kbd>API Methods</kbd></a> &nbsp;•&nbsp; 
	<a href="#resources"><kbd>Resources</kbd></a> &nbsp;•&nbsp; 
    <a href="#names"><kbd>Names</kbd></a>
  </p>
</div>

---

<a id="api-methods"></a>

<div align="center">
	<h2>❮ <code><b>API Methods</b></code> ❯</h2> 
</div>

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

---

<a id="resources"></a>

<div align="center">
  <h2>❮ <code><b>Resources</b></code> ❯</h2> 
</div>

<div align="center">
	<h4><code>Complete sounds list with audio by <i>FrostyCaveman</i></code><br></h4>
	<h4><a href="https://bloxdfc.pages.dev/sounds"><code>bloxdfc.pages.dev/sounds</code></a></h4>
</div>

---

<a id="names"></a>

<div align="center">
	<h2>❮ <code><b>Names</b></code> ❯</h2> 
</div>

<div align="center">
  <table>
    <tbody>
      <tr>
        <td valign="top" align="left">
          <h4 align="center"><code>mobs</code></h4>
          <div align="left">
            <a href="#golem"><code>Golem</code></a><br>
            <a href="#cow"><code>Cow</code></a><br>
            <a href="#pig"><code>Pig</code></a><br>
            <a href="#sheep"><code>Sheep</code></a><br>
            <a href="#deer"><code>Deer</code></a><br>
            <a href="#stag"><code>Stag</code></a><br>
            <a href="#bear"><code>Bear</code></a><br>
            <a href="#gorilla"><code>Gorilla</code></a><br>
            <a href="#dog"><code>Dog</code></a><br>
            <a href="#cat"><code>Cat</code></a><br>
            <a href="#horse"><code>Horse</code></a><br>
            <a href="#zombie"><code>Zombie</code></a><br>
            <a href="#knight"><code>Knight</code></a><br>
            <a href="#skeleton"><code>Skeleton</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>firearm</code></h4>
          <div align="left">
            <a href="#cannon"><code>Cannon</code></a><br>
            <a href="#hit"><code>Hit</code></a><br>
            <a href="#misc"><code>Misc</code></a><br>
            <a href="#pistol"><code>Pistol</code></a><br>
            <a href="#rifle"><code>Rifle</code></a><br>
            <a href="#semiauto"><code>SemiAuto</code></a><br>
            <a href="#shotgun"><code>Shotgun</code></a><br>
            <a href="#submachine"><code>Submachine</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>blocks</code></h4>
          <div align="left">
            <a href="#block-cloth"><code>Cloth</code></a><br>
            <a href="#block-glass"><code>Glass</code></a><br>
            <a href="#block-grass"><code>Grass</code></a><br>
            <a href="#block-gravel"><code>Gravel</code></a><br>
            <a href="#block-sand"><code>Sand</code></a><br>
            <a href="#block-snow"><code>Snow</code></a><br>
            <a href="#block-stone"><code>Stone</code></a><br>
            <a href="#block-wood"><code>Wood</code></a><br>
          </div>
        </td>
      </tr>
      <tr>
        <td valign="top" align="left">
          <h4 align="center"><code>steps</code></h4>
          <div align="left">
            <a href="#step-cloth"><code>Cloth</code></a><br>
            <a href="#step-grass"><code>Grass</code></a><br>
            <a href="#step-gravel"><code>Gravel</code></a><br>
            <a href="#step-sand"><code>Sand</code></a><br>
            <a href="#step-snow"><code>Snow</code></a><br>
            <a href="#step-stone"><code>Stone</code></a><br>
            <a href="#step-wood"><code>Wood</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>general</code></h4>
          <div align="left">
            <a href="#basic"><code>Basic</code></a><br>
            <a href="#notes"><code>Notes</code></a><br>
            <a href="#game-start"><code>Game Start</code></a><br>
            <a href="#firecracker"><code>Firecracker</code></a><br>
          </div>
        </td>
        <td valign="top" align="left">
          <h4 align="center"><code>actions</code></h4>
          <div align="left">
            <a href="#doors"><code>Doors</code></a><br>
            <a href="#chest"><code>Chest</code></a><br>
            <a href="#bucket"><code>Bucket</code></a><br>
            <a href="#hoe"><code>Hoe</code></a><br>
            <a href="#fishing"><code>Fishing</code></a><br>
            <a href="#xp"><code>XP</code></a><br>
          </div>
        </td>
      </tr>
    </tbody>
  </table>
</div>


> [!NOTE]
> You can get a random similar sound when you use common prefix (i.e. remove the numbers from the sound name of your choice).

---

<div align="left">
    <h3>〔 <code><b>general</b></code> 〕</h3> 
</div>

<div align="left">
    <h4>⊂ <code><b>Basic</b></code> ⊃</h4> 
</div>

<a id="basic"></a>

`beep`  
`bow`  
`burp`  
`cashRegister`  
`drink`  
`eat1`  
`equip_leather1`  
`fallsmall` 
`pickUp`   
`levelup`  
`fireBurn`  
`laugh1`  
`laugh2`  
`laugh3`  
`successfulBowHit`  
`sweep6`  

<div align="left">
    <h4>⊂ <code><b>Notes</b></code> ⊃</h4> 
</div>

<a id="notes"></a>

`bass`  
`bassattack`  
`bd`  
`drumSwish1`  
`drumSwish2`   
`harp_pling`  
`hat`  
`lowDrum1`   
`lowDrum2`   
`lowDrum3`  
`snare`  
`sonarBeep`  
`trumpetFlare`  
`trumpetNote1`  
`trumpetNote2`  
`trumpetNote3`  

<div align="left">
    <h4>⊂ <code><b>Game Start</b></code> ⊃</h4> 
</div>

<a id="game-start"></a>

`game_start_countdown_01`  
`game_start_countdown_02`  
`game_start_countdown_03`  
`game_start_countdown_final`  

<div align="left">
    <h4>⊂ <code><b>Firecracker</b></code> ⊃</h4> 
</div>

<a id="firecracker"></a>

`firecracker1`  
`firecracker2`  
`firecracker3`  
`firecracker4`  

---

<div align="left">
    <h3>〔 <code><b>firearm</b></code> 〕</h3> 
</div>

<div align="left">
    <h4>⊂ <code><b>Cannon</b></code> ⊃</h4> 
</div>

<a id="cannon"></a>

`cannonFire1`  
`cannonFire2`  
`cannonFire3`  

<div align="left">
    <h4>⊂ <code><b>Hit</b></code> ⊃</h4> 
</div>

<a id="hit"></a>

`hit1`  
`hit2`  
`hit3` 

<div align="left">
    <h4>⊂ <code><b>Misc</b></code> ⊃</h4> 
</div>

<a id="misc"></a>

`bullet_shell_bounce_general_07`  
`bullet_shell_bounce_general_08`  
`headshot_04`  
`headshot_06`  
`headshot_08`  
`headshot_11`   

<div align="left">
    <h4>⊂ <code><b>Pistol</b></code> ⊃</h4> 
</div>

<a id="pistol"></a>

`pistol_cock_01`  
`pistol_cock_02`  
`pistol_cock_03`  
`pistol_cock_06`  

`pistol_magazine_load_01`  
`pistol_magazine_load_02`  
`pistol_magazine_load_03`  

`pistol_magazine_unload_01`  
`pistol_magazine_unload_02`  
`pistol_magazine_unload_03`  

`pistol_shot_01`  
`pistol_shot_02`  
`pistol_shot_03`  
`pistol_shot_04`  
`pistol_shot_05`  

<div align="left">
    <h4>⊂ <code><b>Rifle</b></code> ⊃</h4> 
</div>

<a id="rifle"></a>

`rifle_cock_01`  
`rifle_cock_02`  

`rifle_magazine_load_01`  
`rifle_magazine_load_02`  
`rifle_magazine_load_03`  

`rifle_magazine_unload_01`  
`rifle_magazine_unload_02`  
`rifle_magazine_unload_04`  

`rifle_shot_01`  
`rifle_shot_02`  
`rifle_shot_03`  
`rifle_shot_04`  

<div align="left">
    <h4>⊂ <code><b>SemiAuto</b></code> ⊃</h4> 
</div>

<a id="semiauto"></a>

`semiAuto_cock_01`  
`semiAuto_cock_02`  
`semiAuto_cock_03`  
`semiAuto_cock_04`  
`semiAuto_cock_05`  

`semiAuto_magazine_load_01`  
`semiAuto_magazine_load_02`  
`semiAuto_magazine_load_03`  
`semiAuto_magazine_load_04`  
`semiAuto_magazine_load_05`  

`semiAuto_magazine_unload_01`  
`semiAuto_magazine_unload_02`  
`semiAuto_magazine_unload_03`  
`semiAuto_magazine_unload_04`  

`semiAuto_first_shot_01`  
`semiAuto_shot_01`  
`semiAuto_shot_02`  
`semiAuto_shot_03`  
`semiAuto_shot_04`  
`semiAuto_shot_05`  
`semiAuto_shot_06`  
`semiAuto_shot_07`  
`semiAuto_shot_08`  
`semiAuto_tail_only_shot_01`  

<div align="left">
    <h4>⊂ <code><b>Shotgun</b></code> ⊃</h4> 
</div>

<a id="shotgun"></a>

`shotgun_cock_01`  
`shotgun_cock_02`  
`shotgun_cock_03`  
`shotgun_cock_04`  
`shotgun_cock_05`  

`shotgun_load_bullet_01`  
`shotgun_load_bullet_02`  
`shotgun_load_bullet_03`  
`shotgun_load_bullet_04`  
`shotgun_load_bullet_05`  
`shotgun_load_bullet_06`  
`shotgun_load_bullet_07`  
`shotgun_load_bullet_08` 

`shotgun_shot_01`  
`shotgun_shot_02`  
`shotgun_shot_03`  
`shotgun_shot_04`  

<div align="left">
    <h4>⊂ <code><b>Submachine</b></code> ⊃</h4> 
</div>

<a id="submachine"></a>

`submachine_cock_01`  
`submachine_cock_02`  
`submachine_cock_03`  
`submachine_cock_04`  

`submachine_magazine_load_01`  
`submachine_magazine_load_02`  
`submachine_magazine_load_03`  
`submachine_magazine_load_04`  

`submachine_magazine_unload_01`  
`submachine_magazine_unload_02`  
`submachine_magazine_unload_03`  

`submachine_first_shot_01`  
`submachine_shot_01`  
`submachine_shot_02`  
`submachine_shot_03`  
`submachine_shot_04`  
`submachine_shot_05`  
`submachine_shot_06`  
`submachine_shot_07`  
`submachine_shot_08`  
`submachine_shot_09`  
`submachine_tail_only_shot_01`  

---

<div align="left">
    <h3>〔 <code><b>mobs</b></code> 〕</h3> 
</div>

<div align="left">
    <h4>⊂ <code><b>Golem</b></code> ⊃</h4> 
</div>

<a id="golem"></a>

`golemGrunt1`  
`golemGrunt2`  
`caveGolem1`  
`caveGolem2`  
`caveGolem3`  
`caveGolem4`  

<div align="left">
    <h4>⊂ <code><b>Cow</b></code> ⊃</h4> 
</div>

<a id="cow"></a>

`cowMoo1`  
`cowMoo2`  
`cowMoo3`  
`cowHurt1`  

<div align="left">
    <h4>⊂ <code><b>Pig</b></code> ⊃</h4> 
</div>

<a id="pig"></a>

`pigOink1`  
`pigOink2`  
`pigOink3`  
`pigOink4`  
`pigOink5`  
`pigHurt1`  
`pigHurt2`  
`pigHurt3`  

<div align="left">
    <h4>⊂ <code><b>Sheep</b></code> ⊃</h4> 
</div>

<a id="sheep"></a>

`sheepBaa1`  
`sheepBaa2`  
`sheepBaa3`  
`sheepBaa4`  
`sheepHurt1`  

<div align="left">
    <h4>⊂ <code><b>Deer</b></code> ⊃</h4> 
</div>

<a id="deer"></a>

`deerGrunt1`  
`deerHurt1`  

<div align="left">
    <h4>⊂ <code><b>Stag</b></code> ⊃</h4> 
</div>

<a id="stag"></a>

`stagGrunt1`  
`stagHurt1`  

<div align="left">
    <h4>⊂ <code><b>Bear</b></code> ⊃</h4> 
</div>

<a id="bear"></a>

`bearRoar1`  
`bearRoar2`  
`bearRoar3`  
`bearRoar4`  
`bearRoar5`  

<div align="left">
    <h4>⊂ <code><b>Gorilla</b></code> ⊃</h4> 
</div>

<a id="gorilla"></a>

`gorillaIdle1`  
`gorillaIdle2`  
`gorillaIdle3`  
`gorillaIdle4`  
`gorillaRoar1`  

<div align="left">
    <h4>⊂ <code><b>Dog</b></code> ⊃</h4> 
</div>

<a id="dog"></a>

`dogBark1`  
`dogBark2`  
`dogBark3`  
`dogGrowl1`  
`dogGrowl2`  
`dogGrowl3`  
`dogHurt1`  
`dogHurt2`  

<div align="left">
    <h4>⊂ <code><b>Cat</b></code> ⊃</h4> 
</div>

<a id="cat"></a>

`catHiss1`  
`catHiss2`  
`catHiss3`  
`catHiss4`  
`catHurt1`  
`catHurt2`  
`catHurt3`  
`catMeow1`  
`catMeow2`  
`catMeow3`  
`catMeow4`  
`catMeow5`  

<div align="left">
    <h4>⊂ <code><b>Horse</b></code> ⊃</h4> 
</div>

<a id="horse"></a>

`horseHurt1`  
`horseHurt2`  
`horseIdle1`  
`horseIdle2`  
`horseIdle3`  

<div align="left">
    <h4>⊂ <code><b>Zombie</b></code> ⊃</h4> 
</div>

<a id="zombie"></a>

`ZombieGrunt1`  
`ZombieGrunt2`  
`ZombieGrunt3`  
`ZombieHurt1`  
`ZombieHurt2`  
`ZombieHurt3`  
`ZombieHurt4`  

<div align="left">
    <h4>⊂ <code><b>Knight</b></code> ⊃</h4> 
</div>

<a id="knight"></a>

`knightGrunt1`  
`knightGrunt2`  
`knightGrunt3`  

<div align="left">
    <h4>⊂ <code><b>Skeleton</b></code> ⊃</h4> 
</div>

<a id="skeleton"></a>

`skeletonRattle1`  
`skeletonRattle2`  
`skeletonRattle3`  
`skeletonRattle4`  

---

<div align="left">
    <h3>〔 <code><b>blocks</b></code> 〕</h3> 
</div>

<div align="left">
    <h4>⊂ <code><b>Cloth</b></code> ⊃</h4> 
</div>

<a id="block-cloth"></a>

`cloth1`  
`cloth2`  
`cloth3`  
`cloth4`  

<div align="left">
    <h4>⊂ <code><b>Glass</b></code> ⊃</h4> 
</div>

<a id="block-glass"></a>

`glass1`  
`glass2`  
`glass3`  

<div align="left">
    <h4>⊂ <code><b>Grass</b></code> ⊃</h4> 
</div>

<a id="block-grass"></a>

`grass1`  
`grass2`  
`grass3`  
`grass4`  

<div align="left">
    <h4>⊂ <code><b>Gravel</b></code> ⊃</h4> 
</div>

<a id="block-gravel"></a>

`gravel1`  
`gravel2`  
`gravel3`  
`gravel4`  

<div align="left">
    <h4>⊂ <code><b>Sand</b></code> ⊃</h4> 
</div>

<a id="block-sand"></a>

`sand1`  
`sand2`  
`sand3`  
`sand4`  

<div align="left">
    <h4>⊂ <code><b>Snow</b></code> ⊃</h4> 
</div>

<a id="block-snow"></a>

`snow1`  
`snow2`  
`snow3`  
`snow4`  
`splash1`  

<div align="left">
    <h4>⊂ <code><b>Stone</b></code> ⊃</h4> 
</div>

<a id="block-stone"></a>

`stone1`  
`stone2`  
`stone3`  
`stone4`  

<div align="left">
    <h4>⊂ <code><b>Wood</b></code> ⊃</h4> 
</div>

<a id="block-wood"></a>

`wood1`  
`wood2`  
`wood3`  
`wood4`  

---

<div align="left">
    <h3>〔 <code><b>steps</b></code> 〕</h3> 
</div>

<div align="left">
    <h4>⊂ <code><b>Cloth</b></code> ⊃</h4> 
</div>

<a id="step-cloth"></a>

`step_cloth1`  
`step_cloth2`  
`step_cloth3`  
`step_cloth4`  

<div align="left">
    <h4>⊂ <code><b>Grass</b></code> ⊃</h4> 
</div>

<a id="step-grass"></a>

`step_grass2`  
`step_grass1`  
`step_grass3`  
`step_grass4`  
`step_grass5`  

<div align="left">
    <h4>⊂ <code><b>Gravel</b></code> ⊃</h4> 
</div>

<a id="step-gravel"></a>

`step_gravel1`  
`step_gravel2`  
`step_gravel3`  
`step_gravel4`  

<div align="left">
    <h4>⊂ <code><b>Sand</b></code> ⊃</h4> 
</div>

<a id="step-sand"></a>

`step_sand2`  
`step_sand3`  
`step_sand4`  
`step_sand5`  

<div align="left">
    <h4>⊂ <code><b>Snow</b></code> ⊃</h4> 
</div>

<a id="step-snow"></a>

`step_snow1`  
`step_snow2`  
`step_snow3`  
`step_snow4`  

<div align="left">
    <h4>⊂ <code><b>Stone</b></code> ⊃</h4> 
</div>

<a id="step-stone"></a>

`step_stone1`  
`step_stone2`  
`step_stone3`  
`step_stone4`  
`step_stone5`  
`step_stone6`  

<div align="left">
    <h4>⊂ <code><b>Wood</b></code> ⊃</h4> 
</div>

<a id="step-wood"></a>

`step_wood1`  
`step_wood2`  
`step_wood3`  
`step_wood4`  
`step_wood5`  
`step_wood6`  

---

<div align="left">
    <h3>〔 <code><b>actions</b></code> 〕</h3> 
</div>

<div align="left">
    <h4>⊂ <code><b>Doors</b></code> ⊃</h4> 
</div>

<a id="doors"></a>
 
`doorClose`  
`doorClose2`  
`doorOpen-bloxd1`  
`doorOpen-bloxd2`  
`trapdoorOpen` 

<div align="left">
    <h4>⊂ <code><b>Chest</b></code> ⊃</h4> 
</div>

<a id="chest"></a>

`chestClose`  
`chestOpen`  

<div align="left">
    <h4>⊂ <code><b>Bucket</b></code> ⊃</h4> 
</div>

<a id="bucket"></a>

`bucketEmpty1`  
`bucketEmpty2`  
`bucketEmpty3`  
`bucketFill1`  
`bucketFill2`  
`bucketFill3`  

<div align="left">
    <h4>⊂ <code><b>Hoe</b></code> ⊃</h4> 
</div>

<a id="hoe"></a>

`hoeTill1`  
`hoeTill2`  
`hoeTill3`  
`hoeTill4`  

<div align="left">
    <h4>⊂ <code><b>Fishing</b></code> ⊃</h4> 
</div>

<a id="fishing"></a>

`caughtFish`  
`reel` 

<div align="left">
    <h4>⊂ <code><b>XP</b></code> ⊃</h4> 
</div>

<a id="xp"></a>

`exp_collect`  
`exp_levelup`  

---

