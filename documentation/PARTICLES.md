---

<div align="center">
  <h1>PARTICLES</h1>
  <p>
    <a href="#api-methods"><kbd>API Methods</kbd></a>
    &nbsp;•&nbsp; <a href="#texture-names"><kbd>Texture Names</kbd></a>
    &nbsp;•&nbsp; <a href="#usage"><kbd>Usage</kbd></a>
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
 * Play particle effect on all clients, or only on some clients if `clientPredictedBy` is specified.
 *
 * @param {TempParticleSystemOpts} options
 * @param {PlayerId} [clientPredictedBy] - Play only on clients where client with playerId clientPredictedBy is not invisible, transparent, or themselves.
 * @returns {void}
 */
playParticleEffect(options, clientPredictedBy)
```

---

<a id="texture-names"></a>

<div align="center">
	<h2>❮ <code><b>Texture Names</b></code> ❯</h2> 
</div>

`bubble`  
`critical_hit`  
`drift`  
`effect_5`  
`generic_2`  
`glint`  
`soul_0`  
`square_particle`  
`heart`  
`z-particle`  

---

<a id="usage"></a>

<div align="center">
	<h2>❮ <code><b>Usage</b></code> ❯</h2> 
</div>

```js
let [x, y, z] = api.thisPos;
y += 1;

api.playParticleEffect({
  dir1: [-1, -1, -1],
  dir2: [1, 1, 1],
  pos1: [x, y, z],
  pos2: [x + 1, y + 1, z + 1],
  texture: "bubble",
  minLifeTime: 0.2,
  maxLifeTime: 0.6,
  minEmitPower: 2,
  maxEmitPower: 2,
  minSize: 0.25,
  maxSize: 0.35,
  manualEmitCount: 20,
  gravity: [0, -10, 0],
  colorGradients: [
    {
      timeFraction: 0,
      minColor: [60, 60, 150, 1],
      maxColor: [200, 200, 255, 1],
    },
  ],
  velocityGradients: [
    {
      timeFraction: 0,
      factor: 1,
      factor2: 1,
    },
  ],
  blendMode: 1,
});
```

---

<a id="extra-info"></a>

<div align="center">
	<h2>❮ <code><b>Extra Info</b></code> ❯</h2> 
</div>

```ts
type TempParticleSystemOpts = {
	texture: string
	minLifeTime: number
	maxLifeTime: number
	minEmitPower: number
	maxEmitPower: number
	minSize: number
	maxSize: number
	gravity: number[]
	velocityGradients: {
		timeFraction: number
		factor: number
		factor2: number
	}[]
	colorGradients: {
		timeFraction: number
		minColor: [number, number, number, number]
		maxColor?: [number, number, number, number]
	}[] | {
		color: [number, number, number]
	}[]
	blendMode: ParticleSystemBlendMode
	dir1: number[]
	dir2: number[]
	pos1: number[]
	pos2: number[]
	manualEmitCount: number
	hideDist: number
}
```

```ts
enum ParticleSystemBlendMode {
	// Source color is added to the destination color without alpha affecting the result
	OneOne = 0,
	// Blend current color and particle color using particle's alpha
	Standard = 1,
	// Add current color and particle color multiplied by particle's alpha
	Add,
	// Multiply current color with particle color
	Multiply,
	// Multiply current color with particle color then add current color and particle color multiplied by particle's alpha
	MultiplyAdd,
}
```

---

