# Third-party notices

SPAM Overlay ships the third-party components below. Their full licence texts are inside every download: the package's
`LICENSES` folder, `runtime\python\LICENSE.txt` with each Python package's own licence file, and `runtime\dotnet\LICENSE.txt`
with `runtime\dotnet\ThirdPartyNotices.txt`. This page is a summary; the texts in the package are the reference.

## Application runtime

| Component | Version | Licence | Full text in the package |
|---|---|---|---|
| Electron | 44.5.1 | MIT | `LICENSES\electron.txt` |
| Chromium (inside Electron) and its components | as shipped by Electron | BSD-3-Clause and others | `LICENSES\chromium.html` |
| Python | 3.12.10 | PSF License Agreement | `runtime\python\LICENSE.txt` |
| .NET runtime | 10.0.12 | MIT, with third-party notices | `runtime\dotnet\LICENSE.txt`, `runtime\dotnet\ThirdPartyNotices.txt` |

## Engine libraries (.NET)

| Component | Version | Licence |
|---|---|---|
| HarmonyX | 2.16.1 | MIT |
| Mono.Cecil | 0.11.6 | MIT |
| MonoMod.Backports | 1.1.2 | MIT |
| MonoMod.Core | 1.3.4 | MIT |
| MonoMod.ILHelpers | 1.1.0 | MIT |
| MonoMod.RuntimeDetour | 25.3.4 | MIT |
| MonoMod.Utils | 25.0.12 | MIT |

Full texts: `LICENSES\engine-libraries.txt`.

## Python packages

| Component | Version | Licence |
|---|---|---|
| UnityPy | 1.25.4 | MIT |
| numpy | 2.2.6 | BSD-3-Clause (bundled libraries listed in its licence file) |
| Pillow | 11.3.0 | MIT-CMU |
| archspec | 0.2.6 | Apache-2.0 or MIT |
| astc-encoder-py | 0.1.12 | MIT |
| attrs | 26.1.0 | MIT |
| Brotli | 1.2.0 | MIT |
| etcpak | 0.9.15 | MIT |
| fmod-toolkit (Python wrapper) | 0.1.3 | MIT |
| fsspec | 2026.9.0 | BSD-3-Clause |
| lz4 | 4.4.5 | BSD-3-Clause |
| pyfmodex | 0.7.2 | MIT |
| texture2ddecoder | 1.0.6 | MIT |
| tpk-ar | 0.2.4 | MIT |
| TypeTreeGeneratorAPI | 0.0.10 | MIT |

Full texts: each package's `*.dist-info` folder under `runtime\python\Lib\site-packages`.

## Fonts

Lilita One (The Lilita One Project Authors) and Nunito (The Nunito Project Authors), SIL Open Font License 1.1, self-hosted Latin
subsets. Full text: `LICENSES\fonts.txt`.

## Not shipped

Npcap is not part of the download: you install it yourself from [npcap.com](https://npcap.com) under its own licence. Nothing of
the game's code or data is shipped; the engine is prepared at the first start from your own copy of the game. SPAM, its name and
its card art belong to their publisher.
