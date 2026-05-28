<p align="center">
  <img src="https://cdn.modrinth.com/data/cached_images/234986ff6803e76844666ecccec7870001878a7e_0.webp" alt="CIT Resewn Continuation Banner">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Loader-Fabric-f16436?style=for-the-badge&logo=fabric&logoColor=white" alt="Fabric">
  <img src="https://img.shields.io/badge/Loader-NeoForge-f28c28?style=for-the-badge" alt="NeoForge">
  <img src="https://img.shields.io/badge/Status-Actively%20Maintained-brightgreen?style=for-the-badge" alt="Actively Maintained">
  <img src="https://img.shields.io/badge/Modpack%20Use-Welcome-brightgreen?style=for-the-badge" alt="Modpack Use Welcome">
  <img src="https://img.shields.io/badge/License-MIT-blue?style=for-the-badge" alt="MIT License">
</p>

<p align="center">
  <a href="https://modrinth.com/mod/cit-resewn-continuation">
    <img src="https://img.shields.io/badge/Available%20on-Modrinth-00AF5C?style=for-the-badge&logo=modrinth&logoColor=white" alt="Modrinth">
  </a>
  <a href="https://www.curseforge.com/minecraft/mc-mods/cit-resewn-continuation">
    <img src="https://img.shields.io/badge/Available%20on-CurseForge-f16436?style=for-the-badge&logo=curseforge&logoColor=white" alt="CurseForge">
  </a>
  <a href="https://github.com/EthanVisagie/CIT-Resewn-Continuation-1.21.11">
    <img src="https://img.shields.io/badge/Source-GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub">
  </a>
  <a href="https://github.com/EthanVisagie/CIT-Resewn-Continuation-1.21.11/issues">
    <img src="https://img.shields.io/badge/Report-Issues-red?style=for-the-badge&logo=github" alt="Issues">
  </a>
</p>

<p align="center">
  <strong>Unofficial continuation of CIT Resewn for modern Minecraft versions on Fabric and NeoForge.</strong>
</p>

# CIT Resewn Continuation

CIT Resewn Continuation keeps MCPatcher and OptiFine-style Custom Item Textures working on newer Minecraft versions where the original CIT Resewn is no longer updated.

It is made for players, resource pack users, and modpack creators who still rely on classic CIT resource packs but want to play on modern Fabric or NeoForge versions without needing OptiFine.

The original CIT Resewn supports versions up to Minecraft 1.21.1. This continuation picks up where it left off by keeping the same CIT resource pack format working on newer Minecraft versions.

## What is CIT Resewn Continuation?

CIT Resewn Continuation lets existing CIT-compatible resource packs keep working on newer Minecraft versions.

It supports custom item textures, custom item models, armor CIT, elytra CIT, and several legacy CIT resource pack features.

Many existing OptiFine-style CIT resource packs should work without needing changes, though some edge cases may still need testing.

## Why use this instead of only vanilla item models?

Minecraft’s newer item model system is useful for datapacks, servers, maps, and mods that can give items custom model data or other components.

CIT is still useful because it supports the classic OptiFine-style workflow where resource packs can react to renamed items and legacy CIT rules. This helps existing packs keep working and keeps name-based custom item textures usable on newer Minecraft versions.

In short:

- Vanilla item models are great for controlled custom items.
- CIT is great for existing OptiFine-style packs and rename-based customization.
- This mod helps keep that older but still-loved workflow alive.

## Supported Minecraft Versions

Currently supported versions include:

### Fabric

- Minecraft 26.1
- Minecraft 26.1.x
- Minecraft 1.21.11
- Minecraft 1.21.10

### NeoForge

- Minecraft 1.21.11 beta
- Minecraft 1.21.10 beta

Supported loaders depend on the release file. Make sure to download the correct jar for your Minecraft version and loader.

More versions are planned and currently being tested.

## What Works

Known working areas include:

- Item model CIT, including custom models for renamed items
- Texture-only CIT, including custom textures for renamed items
- Armor CIT on the modern equipment renderer
- Elytra CIT
- Legacy `CustomModelData` conditions
- Legacy `Damage` NBT conditions
- Legacy item subtexture overrides such as `texture.layer1`
- Model-backed CITs with OptiFine-style relative texture references such as `./texture_name`
- Non-UTF-8 `.properties` files with Latin-1 fallback parsing
- Trident throwing CIT model overrides
- Bow, crossbow, and shield sub-item model overrides
- First-pass enchantment glint CIT support

## NeoForge Status

NeoForge support is currently marked as beta.

Item CIT, texture CIT, model CIT, armor CIT, and elytra CIT have been tested with large real-world CIT resource packs and showcase worlds.

Enchantment glint overrides still need additional testing. Performance may vary in extremely CIT-heavy worlds with many displayed items.

Fabric support is currently more mature. NeoForge support is newer and will continue receiving fixes as more users test it.

## Installation

### Fabric

1. Install Fabric Loader.
2. Install Fabric API.
3. Download the correct CIT Resewn Continuation jar for your Minecraft version.
4. Put the jar in your `mods` folder.
5. Put any CIT-compatible resource pack in your `resourcepacks` folder.
6. Enable the resource pack in-game.

### NeoForge

1. Install NeoForge.
2. Download the correct CIT Resewn Continuation jar for your Minecraft version.
3. Put the jar in your `mods` folder.
4. Put any CIT-compatible resource pack in your `resourcepacks` folder.
5. Enable the resource pack in-game.

The defaults module is bundled inside the main jar when the release is built that way. Do not install a separate defaults jar unless the release notes explicitly tell you to.

## Downloads

Approved builds are available here:

- Modrinth: https://modrinth.com/mod/cit-resewn-continuation
- CurseForge: https://www.curseforge.com/minecraft/mc-mods/cit-resewn-continuation
- GitHub: https://github.com/EthanVisagie/CIT-Resewn-Continuation-1.21.11

Development artifacts may also be available from this repository's GitHub releases page.

## For Modpack Creators

Modpack use is welcome.

This project is intended to help players and modpack creators keep existing CIT resource packs working on newer Minecraft versions.

CIT Resewn Continuation is available on both Modrinth and CurseForge.

Before using a beta NeoForge build in a public modpack, please test it with your resource packs and renderer/shader setup.

If you run into compatibility issues with a resource pack, please open an issue with the pack name, Minecraft version, loader, and logs.

## Performance

This fork includes optimizations over the original CIT Resewn, including reduced unnecessary CIT render work and faster matching for common name patterns.

Recent versions also reduce resource-reload pressure from large CIT packs and harden model loading so malformed CIT model JSON is logged and skipped instead of aborting the entire model reload path.

If you used CIT Resewn on Minecraft 1.21.1 and noticed frame drops, this continuation may be worth trying on newer versions.

NeoForge builds are still being tested and optimized. Normal gameplay should be fine, but extremely CIT-heavy showcase worlds may perform differently than Fabric.

## Known Limits

Some edge-case OptiFine CIT properties may still be incomplete.

Behavior can vary by loader branch and Minecraft version.

Shader, renderer, and resource-pack combinations should be tested before using a build in a public modpack.

Enchantment glint overrides currently have first-pass support and still need broader testing.

## Testing

Useful validation packs and setups include:

- TooManyRenames
- Barely Default
- FurfSky Reborn
- enchantment-heavy CIT packs
- armor and elytra CIT packs
- shader setups such as Complementary Reimagined

If you hit a broken model, missing texture, incorrect CIT match, resource reload issue, or startup crash, please open an issue and include:

- Minecraft version
- loader and loader version
- CIT Resewn Continuation version
- resource pack name and version
- the relevant `.properties` file when possible
- `latest.log` or the crash report

## CIT Docs

Most existing CIT Resewn pack and API docs still apply.

The original docs site is available here:

https://citresewn.shcm.io

## API

The API surface is still based on the original CIT Resewn project.

If this fork is published to a Maven repository later, dependency coordinates and examples will be updated here to match the continuation project.

For normal players and modpack users, only the main jar is needed.

## Contributing

Bug fixes, porting fixes, pack compatibility fixes, and small verified behavior improvements are welcome.

Good contributions include:

- Fixes for specific resource-pack compatibility issues
- Loader-specific fixes
- Performance improvements
- Better logging for broken packs or malformed CIT files
- Documentation improvements
- Reproducible test packs or minimal examples

Please include testing notes when opening a pull request.

## Development Status

This fork is actively maintained for newer Minecraft versions beyond the original CIT Resewn release range.

Recent updates restored legacy `CustomModelData`, `Damage`, subtexture, armor, elytra, model-backed CIT, and non-UTF-8 `.properties` compatibility while also improving matching and render performance.

The goal is to keep existing OptiFine-style CIT packs usable on modern Minecraft versions while preserving the original format as much as possible.

## Credits

CIT Resewn Continuation is an unofficial continuation of [CIT Resewn](https://modrinth.com/mod/cit-resewn) by SHsuperCM.

CIT Resewn is an implementation of MCPatcher's Custom Item Textures. This project would not exist without SHsuperCM's work.

NeoForge support also builds on work from [CIT Reforged](https://modrinth.com/mod/cit-reforged), which helped bring CIT Resewn-style functionality to the Forge ecosystem.

Thank you to the original CIT Resewn, CIT Reforged, MCPatcher, and OptiFine CIT communities for creating and preserving the custom item texture format that so many resource packs still rely on.

## License

CIT Resewn Continuation follows the MIT License, matching the original CIT Resewn project license.

See the `LICENSE` file for details.

## Support

CIT Resewn Continuation is free and open source.

If this mod helped you keep your resource packs working on newer Minecraft versions, support options may be added in the future.

For now, the best way to support the project is to report issues clearly, share reproducible examples, and help test real-world CIT resource packs.

Support helps fuel the caffeine required for porting, testing, debugging cursed mixins, and keeping OptiFine-style CIT alive on modern Minecraft.
