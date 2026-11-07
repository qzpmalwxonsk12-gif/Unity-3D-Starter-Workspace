# Unity 3D Starter Workspace

A preserved Unity starter project containing the initial scene, Universal Render Pipeline configuration and editor setup assets. It is a starting point for future development, not a finished game or a separate SAS4 release.

## Included content

- Unity project settings and a package manifest.
- A sample scene and template rendering/input assets.
- Tutorial/readme editor scripts and a package-resolution helper.
- Generated C# solution/project files retained with the workspace.

There are no custom missions, progression systems or complete gameplay loops in this snapshot. The Unity AI packages listed in the manifest are package dependencies; their presence does not demonstrate a working AI feature in this project.

## Requirements

The checked-in [`ProjectVersion.txt`](ProjectSettings/ProjectVersion.txt) specifies **Unity 6000.6.6f1**. Use that editor version when reproducing the snapshot. Package versions are recorded in [`Packages/manifest.json`](Packages/manifest.json), including the Universal Render Pipeline and Input System.

Unity Hub is a convenient way to select the editor. An IDE is optional for opening the scene, but useful when editing C# scripts. Package restoration may require internet access and any entitlement required by a particular package.

## Open the project

1. Clone or download this repository into a writable directory.
2. In Unity Hub, add the folder containing `Assets`, `Packages` and `ProjectSettings`.
3. Open it with the recorded editor version and allow package import to finish.
4. Open the sample scene under [`Assets/Scenes`](Assets/Scenes) and press Play.

If a template/package component is unavailable, resolve it through Unity's Package Manager before attempting a build. Do not treat a successful package import as proof that a complete game exists.

## Project structure

| Path | Purpose |
|---|---|
| `Assets/` | Scenes, template assets and editor scripts |
| `Packages/` | Dependency manifest and package lock data |
| `ProjectSettings/` | Editor version, rendering, input and build settings |
| `Assets/TutorialInfo/` | Unity template tutorial/readme assets |

`Library`, `Temp` and other generated editor caches are intentionally not part of the source backup. Unity recreates them when the project is imported. The `.csproj` and `.slnx` files are not the authoritative dependency configuration; Unity can regenerate them.

## Build and extend

Choose the desired target in Unity's build settings, add the scene you intend to run, and create a local build. There is no checked-in release executable or documented gameplay acceptance suite for this starter. Add gameplay and tests deliberately rather than assuming template content is production functionality.

## Status and attribution

This is a starter/source snapshot. Documentation was reviewed against its files; no fresh editor or standalone-player test was performed for this README update. Unity and package assets retain their respective licenses and attribution requirements. See [backup notes](BACKUP_NOTES.md) for snapshot exclusions.
