<p align="center">
  <img src="https://citresewn.shcm.io/img/project_description/logo_shadow.png" width="200px">
</p>

<p align="center">
  <a href="https://modrinth.com/mod/cit-resewn-continuation"><img src="https://img.shields.io/badge/Modrinth-CIT%20Resewn%20Continuation-00AF5C?logo=modrinth&logoColor=white" alt="Download on Modrinth"></a>
</p>

# CIT Resewn Continuation

CIT Resewn Continuation is an unofficial community fork of CIT Resewn. It keeps MCPatcher and OptiFine-style Custom Item Texture support available on newer Minecraft versions without requiring OptiFine.

The main module provides the CIT API. The Defaults module provides the standard CIT behavior used by most resource packs.

## Supported Versions

Current continuation builds are published for modern Minecraft versions, including `1.21.10`, `1.21.11`, and `26.1.x` builds where available.

Supported loaders depend on the release file. Use the jar that matches your Minecraft version and loader.

Recent work in this fork includes:

- Minecraft `1.21.11` support
- Minecraft `26.1.x` support
- Fabric and NeoForge continuation builds where available
- item model CIT fixes
- common texture-only item CIT fixes
- armor CIT support
- elytra CIT support
- enchantment glint CIT work
- relative texture path fixes
- trident throwing CIT model override fixes

## Installation

1. Install the loader required by the release file.
2. Install Fabric API or the loader dependencies required by your modpack when applicable.
3. Put the CIT Resewn Continuation jar in your `mods` folder.
4. Launch the game once.
5. Put any CIT-compatible resource pack in `resourcepacks`.
6. Enable the resource pack in-game.

The defaults module is bundled inside the main jar when the release is built that way. Do not install a separate defaults jar unless the release notes explicitly tell you to.

## Downloads

Download approved builds from Modrinth:

https://modrinth.com/mod/cit-resewn-continuation

Development artifacts may also be available from this repository's GitHub releases page.

## Pack Compatibility

This fork is intended to keep existing CIT Resewn and OptiFine-style CIT packs usable on modern loader-based Minecraft installations.

Known working areas include:

- item model CITs
- common texture-only item CITs
- armor CITs
- elytra CITs
- first-pass enchantment glint CITs

Known limits:

- some edge-case OptiFine CIT properties are still incomplete
- behavior can vary by loader branch and Minecraft version
- shader and renderer combinations should be tested before using a build in a public modpack

## Testing

Useful validation packs and setups include:

- TooManyRenames
- enchantment-heavy CIT packs
- Fabulously Optimized
- shader setups such as Complementary Reimagined

If you hit a broken model, missing texture, incorrect CIT match, or startup crash, open an issue and include:

- Minecraft version
- loader and loader version
- CIT Resewn Continuation version
- resource pack name and version
- the relevant `.properties` file when possible
- `latest.log` or the crash report

## CIT Docs

Most existing CIT Resewn pack and API docs still apply. The original docs site is available at:

https://citresewn.shcm.io

## API

The API surface is still based on the original CIT Resewn project. If this fork is published to a Maven repository later, dependency coordinates and examples should be updated here to match the continuation project.

## Contributing

Bug fixes, porting fixes, pack compatibility fixes, and small verified behavior improvements are welcome.

## Credits

CIT Resewn was originally created by SHsuperCM. This continuation keeps the project usable on newer Minecraft versions while preserving the original credits and license terms.
