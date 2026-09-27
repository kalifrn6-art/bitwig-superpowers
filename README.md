# Bitwig Superpowers

Native MIDI Tools and Audio Tools for Bitwig Studio.

This repository is the public download page. The implementation and development
history are private. Installers do not include Bitwig Studio, Bitwig vendor JARs,
license keys, or a Bitwig license. You must use your own valid Bitwig installation
and license.

## Downloads

Both downloads are native graphical installers. The macOS DMG and Windows EXE
include their own Python and reviewed FFmpeg/ffprobe builds. No command launcher,
separate Python installation, or separate FFmpeg installation is needed.
Readable project implementation source is not distributed. Compiled code can
still be reverse-engineered.

Download installers only from the [Releases](https://github.com/kalifrn6-art/bitwig-superpowers/releases)
page. Do not use GitHub's automatically generated “Source code” archives; they
contain only this public download-page README.

### Current beta compatibility

| Platform | Supported Bitwig version | Package |
|---|---:|---|
| macOS 13+ Apple Silicon | 6.1.1 / 6.1.2 / **6.1.3** | [Beta 4.3 DMG](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-4-3/Bitwig-Superpowers-macOS-AppleSilicon-Beta-4.3.dmg) |
| Windows 10/11 x64 | 6.1.1 / **6.1.3** | [Beta 4.3 EXE](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-4-3/Superpowers-Windows-x64-Beta-4.3.exe) |

**Beta 4.3** (macOS and Windows) fixes Capture MIDI on Bitwig 6.1.3: clips now land where you played them instead of at bar 1.1.1, and a capture never replaces an existing clip (it goes to a new track). Install it over Beta 4, 4.1 or 4.2. Read the [Beta 4.3 release notes](https://github.com/kalifrn6-art/bitwig-superpowers/releases/tag/superpowers-beta-4-3).

**Windows Beta 4.2** fixes the Audio Tools setup on Bitwig 6.1.3 (it stopped with `No module named 'install'` and nothing got installed) and adds the Capture MIDI icon. Read the [Beta 4.2 release notes](https://github.com/kalifrn6-art/bitwig-superpowers/releases/tag/superpowers-beta-4-2).

**Beta 4.1** fixes Track Freeze occasionally leaving the audio engine paused; it updates a Beta 4 installation in place. Read the [Beta 4.1 release notes](https://github.com/kalifrn6-art/bitwig-superpowers/releases/tag/superpowers-beta-4-1).

**New in Beta 4 (Bitwig 6.1.3):** right-click an audio clip in the Arranger for
*Separate Stems* and *Audio to MIDI* (Melody, Harmony, Drums), *Capture MIDI*
(retrieve what you just played, from the Play menu or the toolbar button) and
*Track Freeze*. Audio Tools moved from the Inspector to the audio clip menu; MIDI
Tools stay in the Inspector. Earlier Bitwig versions keep the tools of their
previous beta. Read the [Beta 4 release notes](https://github.com/kalifrn6-art/bitwig-superpowers/releases/tag/superpowers-beta-4).

**Capture MIDI tip: if the captured clip looks empty, drag its left edge to the
left.** The clip opens on only the last bars before you clicked Capture, but it
already holds everything you played in the last five minutes, just before its
start. Extending the left edge reveals the earlier notes.

**If something fails, send the installer log.** Every operation is logged:

- macOS: `~/Library/Logs/Bitwig Superpowers/` — the installer offers *Show Log in Finder* and *Copy Log*.
- Windows: `%LOCALAPPDATA%\Bitwig Superpowers\Logs\` — the installer offers *Open installer log*.

The installers detect the installed version and select a reviewed profile.
Analysis and patching implementations remain compiled. Unknown future versions
are not supported automatically. The Mac beta is ad-hoc signed, not Developer ID
signed or notarized; the Windows installer is not code-signed.

These beta installers are version-specific. They deliberately stop on an unknown
or modified Bitwig JAR instead of guessing. Support for a new Bitwig release is
published only after its detected profile and resulting patch have been reviewed
and tested.

During this beta cycle, releases focus on fixes. Each published correction moves
to the next beta number so testers can identify the exact installer they used.

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
helps me maintain and improve the beta. Support is always optional.
[Support Superpowers through Stripe](https://buy.stripe.com/9B64gA1b04jzaJbgyi1Jm00)

Use beta software on backed-up projects. Nothing is uploaded automatically. To
report a problem, open a GitHub issue with your operating system, exact Bitwig
version, installer version, steps to reproduce, and sanitized logs. Never upload
your Bitwig JAR, license data, private projects, credentials, or personal paths.

Bitwig Studio is a product of Bitwig GmbH. This project is independent and is not
affiliated with or endorsed by Bitwig GmbH.
