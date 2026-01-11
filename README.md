---

<div align="center">
  <h1>Bloxd Codex</h1>
  <p>
    <code>extended and organized documentation</code><br>
	<code>maintained by community</code><br>
  </p>
	<p>
	  <a href="#intro"><kbd>Intro</kbd></a>
	  &nbsp;•&nbsp; <a href="#basics"><kbd>Basics</kbd></a>
	  &nbsp;•&nbsp; <a href="#repo-guide"><kbd>Repo Guide</kbd></a>
	  &nbsp;•&nbsp; <a href="#credits"><kbd>Credits</kbd></a>
	</p>
</div>

---

<a id="intro"></a>

<div align="center">
	<h2>👥 ❮ <code><b>Intro</b></code> ❯ 👥</h2> 
</div>

> [!NOTE]<br>
> This is _not_ [the official documentation](https://github.com/Bloxdy/code-api) and is not edited or run by any of Bloxd.io developers.<br>

> [!WARNING]<br>
> This repository may contain out-of-date or incorrect information at times, but maintainers try to keep it as correct and up to date as they can.<br>

> [!TIP]<br>
> Found something that should be added or changed? Please report issue on [discord](https://discord.com/channels/804347688946237472/1457772930443382855) or create a pull request!<br>

> [!IMPORTANT]
> `The JavaScript can interact with the Bloxd.io game API.`<br>
> `You can execute code by right clicking code blocks or using in-game events.`<br>
> `Editing is available only to owners, co-owners, coders of worlds/lobbies.`<br>
> `Please use Bloxd.io's official Discord server to report issues or request features:`<br>
> ➜ [`discord.gg/playbloxd`](https://discord.gg/playbloxd)<br>

---

<a id="basics"></a>

<div align="center">
	<h2>🚩 ❮ <code><b>Basics</b></code> ❯ 🚩</h2> 
</div>

<ol>
  <li>
    <b>Limits</b>
    <ul>
      <li>Both <code>World Code</code> and <code>Code Blocks</code> are limited to <code>16_000</code> characters (including spaces and line breaks).</li>
      <li>The in-game code editor is about <code>~80</code> characters wide.</li>
      <li><code>Code Blocks</code> also have <code>500 lines limit</code> (<code>World Code</code> does not).</li>
    </ul>
  </li>
  <li>
    <b>Variables &amp; Scope</b>
    <ul>
      <li>
        Both <code>World Code</code> and each <code>Code Block</code> run in their own scope (separate
        <a href="https://javascript.info/closure">closure</a>).
      </li>
      <li>
        To share variables between them, put state on the global object:
        <ul>
          <li><code>globalThis.variableName</code> <i>(explicit — recommended)</i></li>
          <li><code>variableName</code> <i>(implicit global)</i></li>
          <li><code>var variableName</code> <i>(implicit global)</i></li>
        </ul>
      </li>
    </ul>
  </li>
  <li>
    <b>Swear filter</b>
    <ul>
      <li>The swear filter applies to <code>Code Blocks</code>, but not to <code>World Code</code>.</li>
    </ul>
  </li>
  <li>
    <b>Execution model</b>
    <ul>
      <li><code>World Code</code> runs once when the lobby is created, and again after code updates (when the world code is re-initialized).</li>
      <li><code>Code Blocks</code> run only when pressed / triggered.</li>
    </ul>
  </li>
  <li>
    <b>Callbacks</b>
    <ul>
      <li>Game events (callback functions like <code>tick</code>, <code>onPlayerJoin</code>, etc.) are wired once during lobby code init ("world code init").</li>
      <li>Because of that, you cannot declare callbacks inside <code>Code Blocks</code> <ins>directly</ins>.</li>
      <li>
        You can change behavior later via delegator pattern:
        <ul>
          <li>declare the real (wired) callback function in <code>World Code</code>,</li>
          <li>and call another function(-s) stored in some shared object (which can be replaced in <code>Code Blocks</code>).</li>
        </ul>
      </li>
    </ul>
  </li>
  <li>
    <b>Triggering Code Blocks</b>
    <ul>
      <li>There is no direct API to run <code>Code Blocks</code> from <code>World Code</code>.</li>
      <li>A workaround is to read block's stored code (data) and <code>eval</code> it to get similar behavior.</li>
    </ul>
  </li>
</ol>


---

<a id="repo-guide"></a>

<div align="center">
	<h2>📚 ❮ <code><b>Repo Guide</b></code> ❯ 📚</h2> 
</div>

<ul>
  <li><code><b><a href="documentation/CODE_API.md">CODE_API</a></b> — core scripting API reference</code></li>
  <li><code><b><a href="documentation/CALLBACKS.md">CALLBACKS</a></b> — game events & callback signatures</code></li>
  <li><code><b><a href="documentation/CLIENT_OPTIONS.md">CLIENT_OPTIONS</a></b> — player client options</code></li>
  <li><code><b><a href="documentation/ENTITY_SETTINGS.md">ENTITY_SETTINGS</a></b> — various entity settings</code></li>
  <li><code><b><a href="documentation/MOB_SETTINGS.md">MOB_SETTINGS</a></b> — mob defaults and behavior tuning</code></li>
  <li><code><b><a href="documentation/ENTITY_MESHES.md">ENTITY_MESHES</a></b> — entity meshes, attachments, types, and options</code></li>
  <li><code><b><a href="documentation/LOBBY_LEADERBOARD.md">LOBBY_LEADERBOARD</a></b> — lobby leaderboard columns, values, rendering, sorting</code></li>
  <li><code><b><a href="documentation/ENCHANTING.md">ENCHANTING</a></b> — enchantments list, attributes, probabilities</code></li>
  <li><code><b><a href="documentation/ITEMS.md">ITEMS</a></b> — items & blocks list (external detailed reference)</code></li>
  <li><code><b><a href="documentation/PARTICLES.md">PARTICLES</a></b> — particle API, textures, and usage</code></li>
  <li><code><b><a href="documentation/SOUNDS.md">SOUNDS</a></b> — sound API, names, and usage</code></li>
  <li><code><b><a href="documentation/MUSIC.md">MUSIC</a></b> — music client option names and usage</code></li>
  <li><code><b><a href="documentation/SKINS.md">SKINS</a></b> — cosmetic skins and player appearance</code></li>
  <li><code><b><a href="documentation/POSES_AND_STATES.md">POSES &amp; STATES</a></b> — player poses and physics states</code></li>
  <li><code><b><a href="documentation/ICONS.md">ICONS</a></b> — UI icon names supported by bloxd</code></li>
</ul>

---

<a id="credits"></a>

<div align="center">
	<h2>📜 ❮ <code><b>Credits</b></code> ❯ 📜</h2> 
</div>

<ul>
  <li>
    <code><b><a href="https://github.com/tom288">Tom</a></b> — Bloxd.io developer</code><br>
     ➜ <code><a href="https://github.com/Bloxdy/code-api">Bloxdy/code-api</a></code>
  </li>
  <li>
    <code><b><a href="https://github.com/Sheriff-Unit-3">Sheriff U3</a></b> — community contributor</code><br>
     ➜ <code><a href="https://github.com/Sheriff-Unit-3/Bloxd.io-API-code">Bloxd.io-API-code</a></code>
  </li>
</ul>

---

