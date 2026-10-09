<div align="center">

# PureScale Modern

**Upscaling and frame generation for Minecraft.**

![Version](https://img.shields.io/badge/version-1.2-72a7ff?style=flat-square)
![Minecraft](https://img.shields.io/badge/Minecraft-1.7.10_to_26.3-67b96b?style=flat-square)
![Loaders](https://img.shields.io/badge/loaders-Fabric_%2F_NeoForge_%2F_Forge-d6b26b?style=flat-square)

[Download](https://github.com/XsoraS/purescale/releases) · [Discord](https://discord.gg/XgH4EpyPD2) · [Video](https://www.youtube.com/watch?v=xIIHwB45ZEw)

</div>

PureScale renders the game at a lower resolution and rebuilds it at your screen resolution. The HUD and menus stay native, so inventory text and icons stay crisp.

Modern adds DLSS Super Resolution, DLSS Frame Generation and FSR 4.1 alongside the built-in upscalers. It works through the mod and its native runtimes, with no ReShade setup. The built-in modes can run without those extra downloads; vendor modes need a compatible GPU and runtime.

Start with Quality and see how it feels. You can spend an afternoon adjusting everything, but picking a mode and getting back to the game is fine too. It helps most when your GPU is doing the heavy lifting, especially at higher resolutions or with shaders.

## Pick your build

| Minecraft | Fabric | NeoForge | Forge |
| --- | --- | --- | --- |
| 1.7.10 | - | - | [Forge](mods/forge/purescale-modern-1.2-forge-mc1.7.10.jar) |
| 1.8 | - | - | [Forge](mods/forge/purescale-modern-1.2-forge-mc1.8.jar) |
| 1.8.9 | - | - | [Forge](mods/forge/purescale-modern-1.2-forge-mc1.8.9.jar) |
| 1.20.1 | [Fabric](mods/fabric/purescale-modern-1.2-fabric-mc1.20.1.jar) | [NeoForge](mods/neoforge/purescale-modern-1.2-neoforge-mc1.20.1.jar) | [Forge](mods/forge/purescale-modern-forge-mc1.20.1-1.2.jar) |
| 1.21.1 | [Fabric](mods/fabric/purescale-modern-1.2-fabric-mc1.21.1.jar) | [NeoForge](mods/neoforge/purescale-modern-1.2-neoforge-mc1.21.1.jar) | [Forge](mods/forge/purescale-modern-forge-mc1.21.1-1.2.jar) |
| 1.21.11 | [Fabric](mods/fabric/purescale-modern-1.2-fabric-mc1.21.11.jar) | [NeoForge](mods/neoforge/purescale-modern-1.2-neoforge-mc1.21.11.jar) | - |
| 26.1.x | [Fabric](mods/fabric/purescale-modern-1.2-fabric-mc26.1.jar) | [NeoForge](mods/neoforge/purescale-modern-1.2-neoforge-mc26.1.jar) | - |
| 26.2 | [Fabric](mods/fabric/purescale-modern-1.2-fabric-mc26.2.jar) | [NeoForge](mods/neoforge/purescale-modern-1.2-neoforge-mc26.2.jar) | - |
| 26.3 | [Fabric](mods/fabric/purescale-modern-1.2-fabric-mc26.3.jar) | [NeoForge](mods/neoforge/purescale-modern-1.2-neoforge-mc26.3.jar) | - |

Fabric needs Fabric API and Sodium. NeoForge needs Sodium on 1.21.1 and newer, and Embeddium on 1.20.1. Forge 1.20.1 also needs Embeddium; Forge 1.21.1 uses the standard renderer.

The 1.20.1 NeoForge build uses Forge-compatible metadata, so download services may identify it as Forge. The separate Forge build is in the Forge column.

Use Java 17 for 1.20.1, Java 21 for 1.21.x, and Java 25 for 26.x. Install one PureScale edition per instance.

## Install

1. Put the matching JAR in your instance's `mods` folder and add the dependencies above.
2. Start Minecraft and press **F9**.
3. Choose an upscaler. For a native mode, click **Get** to download its runtime. Progress appears as a percentage.
4. Restart after the runtime has finished installing.

If you prefer to install it yourself, download the matching runtime ZIP from [Releases](https://github.com/XsoraS/purescale/releases) and extract it into `purescale_natives` inside the game instance. Keep the subfolders in place. [Runtime packages](NATIVE-PACKAGES.md) lists the exact files.

## Download native runtimes

| Runtime | Direct download |
| --- | --- |
| DLSS Super Resolution | [Download DLSS SR for Windows x64](https://github.com/XsoraS/purescale/releases/latest/download/purescale-modern-dlss-win64.zip) |
| DLSS Frame Generation | [Download DLSS SR + FG for Windows x64](https://github.com/XsoraS/purescale/releases/latest/download/purescale-modern-dlss-fg-win64.zip) |
| FSR 4.1 | [Download FSR 4.1 for Windows x64](https://github.com/XsoraS/purescale/releases/latest/download/purescale-modern-fsr41-win64.zip) |
| Neural Rendering | [Download the experimental NR runtime for Windows x64](https://github.com/XsoraS/purescale/releases/latest/download/purescale-modern-dlss-nr-win64.zip) |

Extract the chosen ZIP into `purescale_natives` inside your Minecraft instance, preserving its subfolders, then restart. The FG package includes the SR runtime too, so you do not need both ZIPs.

These links use the latest published release. If an asset is missing there, check [all releases](https://github.com/XsoraS/purescale/releases) or use **Get** in-game.

## Native features

| Feature | Requirements |
| --- | --- |
| DLSS Super Resolution / DLAA | Compatible NVIDIA RTX GPU, DLSS runtime and OpenGL backend |
| DLSS Frame Generation | Compatible NVIDIA GPU, driver and FG runtime; backend support varies by build |
| FSR 4.1 | Compatible Radeon GPU and FSR runtime |
| Neural Rendering | Optional experimental runtime and compatible hardware |

The supplied native runtimes are for **Windows x64**. Unsupported modes fall back to a built-in upscaler. Selecting DLSS does not guarantee that DLSS is actually running; check the status and log if the image looks unchanged. DLSS SR can fall back on Vulkan.

Neural Rendering is experimental. It is not a promise of full DLSS 5 support, and pass count alone does not prove that the native feature is active. FSR 4.1 output still needs Radeon hardware validation.

## Settings that stay out of the way

The F9 panel keeps the game visible around it. Blur stays inside the rounded panel, with a background opacity of 170/255. Scrolling content fades at both edges, and the cards are a little darker so the sections are easier to read.

Advanced Settings now has a drawn arrow instead of a font symbol. The title, accent and arrow are centered, with slightly less padding throughout. Normal and Modern use the same spacing.

Native Hand was also fixed on the shared 1.21 rendering path. Real and generated frames were compared in-game on 1.21.8, 1.21.10 and 1.21.11; the hand stayed visible with matching lighting. Those checks cover that rendering path, rather than every shader or native FG setup.

## If something looks wrong

Check the game version, loader and required renderer first. For shader problems, try the same scene without the shader pack once. For native modes, check the selected backend and runtime status too.

Send the Minecraft version, loader, GPU, driver, PureScale settings and relevant log when reporting a problem. A screenshot of F9 helps a lot.

## License

PureScale's original work is covered by [CC0 1.0](LICENSE.md). NVIDIA and AMD binaries keep their own licenses. See [third-party notices](THIRD-PARTY-NOTICES.md) and [licenses](licenses).
