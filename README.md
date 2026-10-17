# Bitwig Superpowers

Native MIDI Tools and Audio Tools for Bitwig Studio.

This repository is the public download page. The implementation and development
history are private. Installers do not include Bitwig Studio, Bitwig vendor JARs,
license keys, or a Bitwig license. You must use your own valid Bitwig installation
and license.

**Superpowers is free and made by one person.** If it helps your music, please
[support the project](https://buy.stripe.com/9B64gA1b04jzaJbgyi1Jm00). It keeps new tools coming.

Website and feature tour: [kalifrn.com/superpowers](https://kalifrn.com/superpowers/)

## Downloads

macOS and Windows are native graphical installers with their own Python and
reviewed FFmpeg/ffprobe builds; no separate Python or FFmpeg is needed. Linux is a
small command-line installer. Readable project implementation source is not
distributed. Compiled code can still be reverse-engineered.

Download installers only from the [Releases](https://github.com/kalifrn6-art/bitwig-superpowers/releases)
page. Do not use GitHub's automatically generated "Source code" archives; they
contain only this public download-page README.

### Superpowers Beta 5.0.2 (Bitwig 6.1.5)

| Platform | Bitwig | Package |
|---|---|---|
| macOS 13+ Apple Silicon | **6.1.5** | [Beta 5.0.2 DMG](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-5.0.2/Bitwig-Superpowers-macOS-AppleSilicon-Beta-5.0.2.dmg) |
| Windows 10/11 x64 | **6.1.5** | [Beta 5.0.2 EXE](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-5.0.2/Superpowers-Windows-x64-Beta-5.0.2.exe) |
| Linux x64 (.deb, system or manually unpacked folder) | **6.1.5** | [Beta 5.0.2 tar.gz](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-5.0.2/Superpowers-Linux-x64-Beta-5.0.2.tar.gz) |

Install it over Beta 5 or 5.0.1; no need to restore first. Read the
[Beta 5.0.2 release notes](https://github.com/kalifrn6-art/bitwig-superpowers/releases/tag/superpowers-beta-5.0.2).
From now on new versions support **Bitwig 6.1.5 and later** only. On Bitwig 6.1.3 / 6.1.4 keep
[Beta 5](https://github.com/kalifrn6-art/bitwig-superpowers/releases/tag/superpowers-beta-5)
(it still has Cmd+3, see below); 6.1.1 / 6.1.2 keep Beta 4.3.

**Fixed in 5.0.2**

- **Projects that would not open** ("Unknown enum value with id 7 for enum quantize_grid_subdivision",
  [#19](https://github.com/kalifrn6-art/bitwig-superpowers/issues/19)): projects saved with a 5T / 7T
  grid failed to load. The cause was the Cmd+3 straight / triplet toggle, which is now **removed**;
  the grid works exactly like stock Bitwig again. Your projects were never damaged.
- **Shortcuts you can change:** Collapse / Expand Device and Collapse / Expand Track are now listed in
  Settings > Shortcuts. Remap or remove their keys there; the defaults (`-`, `+` / `=`, Left, Right)
  no longer override your choice.

**New in Beta 5** (also in 5.0.2)

- **Capture MIDI:** keeps the last 30 seconds you played; each capture uses up the buffer, so the next one never repeats notes.
- **Freeze:** one progress window for the whole queue, no repeated missing-plug-in prompts, clips keep their shape with hatched tails, Unfreeze waits until plug-ins reload, 24-bit renders.
- **Export with Group, Return and Master effects:** a new option in Export Audio.
- **Ramp:** Start / End velocity under the Velocity lane of the piano roll.
- **Piano roll:** selection follows moved notes, Cmd+E splits at the grid and keeps the pieces selected, Duplicate copies the full length. (Beta 5 also had Cmd+3 straight / triplet, removed in 5.0.2.)
- **Detect Event Key:** right-click an audio clip; its key is added to the clip name.
- **Device Keys:** `-` collapses the selected device, `+` / `=` expands it.
- **Groups:** lighter group summaries, a compact height toggle, Left / Right fold and unfold tracks, visible Shift ranges.
- **Linux** support (Bitwig 6.1.5).

**Something not working? Use Send Report.** Every installer has it (Linux:
`python3 superpowers_linux.py report`). It saves a zip with your logs on the
Desktop, with your user name and folders removed, and opens a prefilled GitHub
issue. Drag the zip in and submit. Nothing is sent automatically.

The installers check your exact Bitwig version and stop on an unknown or modified
Bitwig JAR instead of guessing. The Mac app is ad-hoc signed, not Developer ID
signed or notarized; the Windows EXE is not code-signed.

## Before installing

Save your projects and fully quit Bitwig Studio, its audio engine, and plug-in
hosts. Keep the installer for access to its restore tools. The installer verifies
the target and creates a verified backup
before replacing anything.

The optional Audio Tools setup downloads pinned Python packages and optional
models over outbound HTTPS. If the Microsoft Visual C++ x64 runtime is missing,
the Windows installer downloads Microsoft's signed installer and shows its normal
license UI. No inbound firewall rule is required.

## Safety and support

If these tools help your music, consider supporting the project. Your support
helps me maintain and improve Superpowers. Support is always optional.
[Support Superpowers through Stripe](https://buy.stripe.com/9B64gA1b04jzaJbgyi1Jm00)

Use beta software on backed-up projects. Nothing is uploaded automatically. To
report a problem, open a GitHub issue with your operating system, exact Bitwig
version, installer version, steps to reproduce, and sanitized logs. Never upload
your Bitwig JAR, license data, private projects, credentials, or personal paths.

Bitwig Studio is a product of Bitwig GmbH. This project is independent and is not
affiliated with or endorsed by Bitwig GmbH.
