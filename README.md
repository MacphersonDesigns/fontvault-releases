# FontVault for testers

FontVault is a font manager for designers. It finds the fonts scattered across your folders and drives, lets you browse and group them, and turns them on for your apps when you need them.

This is a pre-release build shared for testing. Please do not pass it on.

## What it does to your fonts

- It reads font folders where they are. It never moves, renames or deletes a font file.
- It adds one hidden folder, `.fontvault`, inside each library folder you add. That folder holds the index and your collections.
- Activating a font copies it into a FontVault folder inside your own font folder. Deactivating removes only those copies.
- Your fonts are not uploaded anywhere. The app contacts GitHub to check for updates and Google Fonts to load the typefaces of its own interface.

## Install on a Mac

Needs macOS 11 or later.

1. Download `FontVault-mac.zip` from the [FontVault releases page](https://github.com/MacphersonDesigns/fontvault-releases/releases).
2. Unzip it and drag FontVault into your Applications folder. Updates only work from a folder you can write to, so do not run it from Downloads.
3. Open FontVault. macOS blocks it the first time, because the app is not yet signed with an Apple Developer ID. Click Done.
4. Open System Settings, choose Privacy & Security, and scroll down to Security. Next to the message about FontVault, click Open Anyway and confirm.

You only do steps 3 and 4 once. On macOS 14 or earlier, right-click the app and choose Open instead.

## Install on Windows

1. Download `FontVault-windows.zip` from the [FontVault releases page](https://github.com/MacphersonDesigns/fontvault-releases/releases).
2. Unzip the whole folder somewhere you can write to, such as Documents, and run `FontVault.exe`.
3. If Windows shows a "Windows protected your PC" message, choose More info, then Run anyway.

Font activation has not been tested on Windows yet. Please report what you see.

## First five minutes

1. Open Font Library and press the + next to LIBRARIES. Choose a folder of fonts and press Add & Scan.
2. Click a family, then Activate on one style. Check that the font appears in your design app. It can take around ten seconds; if an app that was already open does not show it, restart that app.
3. Make a collection, add a few fonts to it, and press Activate collection.
4. Open Active on this computer and press Deactivate all.

## Updating

The bottom of the sidebar shows the version and a Check for updates link. When a newer version exists the link becomes Update to, followed by the version. The app downloads it, checks it, replaces itself and restarts.

## What to send back

For anything that goes wrong or feels awkward, tell Alex:

- what you did, what you expected, and what happened
- your macOS or Windows version, and the FontVault version from the sidebar
- the log file: `~/Library/Application Support/FontVault/Index/fontvault.log` on a Mac, `%APPDATA%\FontVault\Index\fontvault.log` on Windows

## Removing it

1. In FontVault, open Active on this computer and press Deactivate all.
2. Quit FontVault and delete the app.
3. To remove its data as well, delete `~/Library/Application Support/FontVault` and `~/.fontvault` on a Mac, or `%APPDATA%\FontVault` and the `.fontvault` folder in your user folder on Windows.
4. To remove the index from a font folder, delete the hidden `.fontvault` folder inside it.

## Licence

FontVault is proprietary software, copyright 2026 Alex Macpherson, all rights reserved. Testing it does not give you or your employer any rights in it. The full terms are in the LICENSE file.
