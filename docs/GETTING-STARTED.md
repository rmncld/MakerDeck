# Getting started with MakerDeck

MakerDeck 0.1.0.0 has been submitted to the Elgato Marketplace for review. These instructions describe setup after the plugin becomes available there.

## 1. Install and add your keys

Install MakerDeck through the Elgato Marketplace once published. In Stream Deck, drag MakerDeck actions onto your preferred keys. Start with Dev Setup, Workspace, My Plugins, New Plugin and Plugin Check.

No default profile is included. Arrange the actions to suit your device and workflow.

## 2. Prepare the environment

Press **Dev Setup**. MakerDeck checks Node.js, npm and the Elgato CLI and installs missing tools. Follow any Windows installation prompts and wait for the key to show **READY**. The dedicated Node.js and Elgato CLI keys display their detected versions and status.

Windows Terminal is required for terminal workflows. Install Visual Studio Code if you want to use Open VS Code; Dev Setup's automatic tool installation covers Node.js, npm and the Elgato CLI.

## 3. Set your workspace

Use Workspace's settings to choose your development folder. If no folder is configured, MakerDeck creates and uses `Documents/StreamDeckPlugins`. Press Workspace to open the folder.

Use New Plugin to launch the official Elgato creation wizard, or work with existing plugin projects in your workspace.

## 4. Select the active project

My Plugins displays the active project. Press it to cycle through discovered projects or select a project in its settings.

Project actions use this selection. Merely opening another folder in VS Code does not change MakerDeck's active project. Check My Plugins before running a command.

## 5. Develop and inspect

- **Open VS Code** opens the selected project.
- **Build** runs its build command.
- **Watch** runs watch mode as you edit.
- **Link / Unlink** connects the development plugin to Stream Deck or removes that link.
- **Restart** restarts the selected plugin.
- **Plugin Check** checks the project and environment and writes an HTML report to `.makerdeck/plugin-check/` within that project.
- **Debug** helps investigate the project and its logs.

Plugin Check reports are generated files. If you version your own project, you can exclude `.makerdeck/` in its `.gitignore`. Deleting a report folder does not disable Plugin Check; the next inspection recreates it.

## 6. Validate and package

Run Validate and resolve any reported problems. Run Package to create the distributable `.streamDeckPlugin` file.

Building and packaging a project do not automatically replace a separately installed copy in Stream Deck. Install the new package when testing the distributed version, and distinguish that installed copy from a linked development project.

## If something goes wrong

Check the active project, tool status and terminal output first. A project must provide the scripts required by Build and Watch. Use Plugin Check and Debug to gather useful information, then follow [SUPPORT.md](SUPPORT.md).
