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

### Superpowers Beta 5

| Platform | Beta 5 tools on Bitwig | Older Bitwig | Package |
|---|---|---|---|
| macOS 13+ Apple Silicon | **6.1.3 / 6.1.4 / 6.1.5** | 6.1.1 / 6.1.2 keep Beta 4.3 tools | [Beta 5 DMG](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-5/Bitwig-Superpowers-macOS-AppleSilicon-Beta-5.dmg) |
| Windows 10/11 x64 | **6.1.3 / 6.1.5** | 6.1.1 keeps Beta 4.3 tools | [Beta 5 EXE](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-5/Superpowers-Windows-x64-Beta-5.exe) |
| Linux x64 (.deb, system or manually unpacked folder) | **6.1.5** | — | [Beta 5 / installer 5.0.1 tar.gz](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-5/Superpowers-Linux-x64-Beta-5.0.1.tar.gz) |

Install it over Beta 4, 4.1, 4.2 or 4.3; no need to restore first. Read the
[Beta 5 release notes](https://github.com/kalifrn6-art/bitwig-superpowers/releases/tag/superpowers-beta-5).

**Linux installer 5.0.1 hotfix (2026-10-17):** fixes `./install.sh --bitwig …`
running status instead of install, and false running-app detection. Finds custom
folders, including .deb files unpacked on Fedora. For a user-owned installation:
`./install.sh --bitwig "$HOME/.applications/bitwig-native/opt/bitwig-studio"`.
Theme-modified JARs require a verified official backup next to `bitwig.jar`; the
modified JAR is preserved separately and the theme is not carried over. Without
that backup, restore official Bitwig first. Reapplying themes is unverified and
may overwrite Superpowers changes. Tested offline using real Linux 6.1.5 files;
interactive Linux validation remains pending. [Installation guide](https://kalifrn.com/superpowers/changelog/#linux).

**New in Beta 5**

- **Capture MIDI:** keeps the last 30 seconds you played; each capture uses up the buffer, so the next one never repeats notes.
- **Freeze:** one progress window for the whole queue, no repeated missing-plug-in prompts, clips keep their shape with hatched tails, Unfreeze waits until plug-ins reload, 24-bit renders.
- **Export with Group, Return and Master effects:** a new option in Export Audio.
- **Ramp:** Start / End velocity under the Velocity lane of the piano roll.
- **Piano roll:** selection follows moved notes, Cmd+E splits at the grid and keeps the pieces selected, Cmd+3 toggles straight / triplet, Duplicate copies the full length.
- **Detect Event Key:** right-click an audio clip; its key is added to the clip name.
- **Device Keys:** `-` collapses the selected device, `+` / `=` expands it.
- **Groups:** lighter group summaries, a compact height toggle, Left / Right fold and unfold tracks, visible Shift ranges.
- **Linux** support (Bitwig 6.1.5) and **Bitwig 6.1.4 / 6.1.5** support on macOS.

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
