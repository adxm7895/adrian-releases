<div align="center">

# ✦ Adrian

### Describe it once. Adrian builds it — on your machine.

**The local-first AI software-creation OS.** Type one sentence and watch it plan, design, code, test, and preview a working app — running on your own hardware, with your own models, for free.

<br/>

<a href="https://github.com/adxm7895/adrian-releases/releases/latest">
<img src="https://img.shields.io/badge/Download_for_Windows-0a0a0a?style=for-the-badge" alt="Download Adrian for Windows" height="44"/>
</a>

<br/><br/>

[![Website](https://img.shields.io/badge/adrianlabs.io-111827?style=flat-square)](https://adrianlabs.io)
[![Web launching soon](https://img.shields.io/badge/web-launching_soon-b45309?style=flat-square)](https://adrianlabs.io)
[![Platform](https://img.shields.io/badge/Windows_10_and_11-0a0a0a?style=flat-square)](https://github.com/adxm7895/adrian-releases/releases/latest)
[![Local and BYOK free forever](https://img.shields.io/badge/local_and_your_keys-free_forever-16a34a?style=flat-square)](#pricing-that-doesnt-punish-you)

<!--
  ▲ VIRAL MONEY-SHOT GOES HERE ▲
  A repo lives or dies on the first thing people see. Record a 10-20s screen
  capture of typing "build me a snake game" and the working app appearing,
  save it as a .gif or .mp4, drag the file into this README on GitHub (it
  uploads and gives you a user-images URL), then paste that URL below:

  ![Adrian in action](PASTE_THE_UPLOADED_GIF_URL_HERE)
-->

</div>

---

> **Adrian is in beta.** It's brand new, so you may run into rough edges or bugs. If you do, please report them to **[info@adrianlabs.io](mailto:info@adrianlabs.io)** — every report goes straight to the people building Adrian and makes the next release better.

## Type one sentence. Get a working app.

```text
"build me a snake game"

  ├─ Plan     detects the app type and shows you the feature scope before it builds
  ├─ Design   a designer agent writes a real spec — palette, layout, components
  ├─ Code     a coder agent writes the app; follow-ups are surgical patch-edits
  ├─ Test     a compile gate + self-review that scores the build and fixes thin ones
  └─ Ship     live preview in-app — then export a zip or deploy it
```

Then just keep talking to it: *"add a high-score board"* — Adrian **edits the existing code** instead of regenerating it, hot-reloads the preview, and **remembers the whole conversation even when you switch models mid-build.**

---

## What actually makes Adrian different

| | **Adrian** | Typical AI builders |
|---|---|---|
| **Where your code runs** | Your machine. Every file, every model, every project. | Their servers. |
| **The free tier** | Local models **+ your own API keys — free forever, no card.** | Credits that run out mid-build. |
| **Weak model?** | A booster pipeline that makes small local models punch above their weight. | You get whatever the model gives you. |
| **Switching models** | Local ⇄ your keys ⇄ hosted Adrian Agents — **mid-conversation, context carries over.** | One vendor, one bill, start over. |
| **When a build fails** | A self-repair loop, plus honest attribution of *which* model failed and *why*. | "Something went wrong." |
| **Does it learn?** | Every correction and failure becomes a lesson it applies to your next build. | It forgets. |

---

## What's under the hood

- **🧠 A real multi-agent pipeline** — separate planner, designer, and coder agents, not one prompt pretending to be a team. Each stage is inspectable.
- **⚡ The booster** — a prompt + context pipeline that gets more out of a small local model than it would produce on its own, so modest hardware still ships real builds.
- **🔁 Context that survives model switches** — start on a local model, finish on Claude or a hosted Adrian Agent; the full conversation and your project come with you.
- **🛠️ Surgical edits, not regeneration** — follow-up requests patch the existing files and hot-reload, so your app evolves instead of resetting every turn.
- **✅ A compile gate + self-review** — generated code is checked and scored before you see it; thin or broken builds get repaired automatically.
- **🔌 Bring any model** — local models via Ollama, or your own keys for **OpenAI, Anthropic, Google, OpenRouter, DeepSeek, and NVIDIA** (plus any custom OpenAI-compatible endpoint).

---

## Local-first, and private by default

Your code, your models, and your API keys **live on your machine and never leave it.**

- API keys are **encrypted in your OS keychain** — never uploaded, never sitting in a config file.
- Generated apps run in an **isolated, sandboxed preview**, jailed to their own folder.
- **No account required** to build with local models or your own keys.

Adrian is local-first by architecture, not by policy.

---

## Pricing that doesn't punish you

- **Free forever** — local models + your own API keys. No card, no credits, no expiry.
- **Adrian Agents (optional)** — add hosted, ready-to-run agents anytime, straight from the app. Your code still stays on your machine.

The desktop app is the free, local-first way in. [adrianlabs.io](https://adrianlabs.io) has the details.

---

## Two ways to run it

- **🖥️ Desktop (this download)** — the full local-first experience: build with local models and your own keys, free forever. Your code and keys never leave your device.
- **🌐 Web — launching soon.** Building in the browser (nothing to install, powered by Adrian Agents) is on the way. Grab the desktop app now; the web is coming shortly — watch [adrianlabs.io](https://adrianlabs.io).

---

## Download & verify

Grab either one from the [**latest release**](https://github.com/adxm7895/adrian-releases/releases/latest):

- **`Adrian-Setup` installer (`.exe`) — recommended.** One install, Start-menu entry, desktop shortcut, uninstaller, **in-place auto-updates**. Prefer this so you don't end up with multiple unzipped copies.
- **`Adrian-Windows.zip` — portable.** No admin. Unzip **once** to a fixed folder and reuse it — the zip does not auto-update, and each extra extract is a whole separate Adrian.

> Windows SmartScreen may warn on a new publisher — click **More info → Run anyway**.
> *(The build is currently unsigned; code signing is on the way. Until then, verify the checksum below.)*

**Verify your download** (recommended):

```powershell
Get-FileHash .\Adrian-Setup-0.1.1.exe -Algorithm SHA256
# or, for the portable zip:
Get-FileHash .\Adrian-Windows.zip -Algorithm SHA256
```

On the [release page](https://github.com/adxm7895/adrian-releases/releases/latest), expand **Assets** — GitHub shows a **SHA-256 next to each file**. Confirm the value above matches the one shown for the exact file you downloaded (each asset has its own hash). This proves the file wasn't tampered with in transit.

---

## Security

- **Hardened runtime.** The packaged binary has Electron fuses flipped that block the classic bypasses: running the app as a plain Node process, injecting code via `NODE_OPTIONS`, and attaching a debugger/inspector. Session cookies are encrypted at rest.
- **Your keys stay yours.** Encrypted in your OS keychain, never uploaded.
- **Sandboxed builds.** Generated apps run in an isolated preview, jailed to their own folder.

Code signing (which removes the SmartScreen warning) is coming; until then the app is unsigned — always verify the SHA-256 above.

---

## FAQ

**Do I need an account or a credit card to start?**
No. Local models and your own API keys are free forever, with no account required.

**Does my code get uploaded anywhere?**
No. With local models and your own keys, everything runs and stays on your machine.

**Which models can I use?**
Local models through Ollama, or your own keys for OpenAI, Anthropic, Google, OpenRouter, DeepSeek, and NVIDIA — plus any custom OpenAI-compatible endpoint. You can switch between them mid-conversation.

**Windows only?**
The current download is for Windows 10 and 11. A browser-based version, **Adrian Web, is launching soon** at [adrianlabs.io](https://adrianlabs.io).

**Is Adrian finished?**
No — it's in **beta**. It works, but expect some rough edges, and please report anything you hit (see below). Your feedback directly shapes what ships next.

---

## Get involved & get in touch

Adrian is in **beta** and built by a small team — your input genuinely shapes where it goes.

- **🐛 Found a bug or something broken?** Email **[info@adrianlabs.io](mailto:info@adrianlabs.io)** with what you were doing and what happened. Beta reports go straight to the people building Adrian.
- **💸 Want to invest?** Adrian is open to investors — reach out at **[info@adrianlabs.io](mailto:info@adrianlabs.io)**.
- **❤️ Want to support the project?** If Adrian is useful to you and you'd like to donate or chip in, get in touch at **[info@adrianlabs.io](mailto:info@adrianlabs.io)**.

---

<div align="center">

**This repo hosts the public Windows releases. The product lives at [adrianlabs.io](https://adrianlabs.io).**

### ⭐ Star this repo if you think local-first AI should beat the cloud.

<br/>

<a href="https://github.com/adxm7895/adrian-releases/releases/latest">
<img src="https://img.shields.io/badge/Get_Adrian_for_Windows-0a0a0a?style=for-the-badge" alt="Download Adrian" height="40"/>
</a>

</div>
