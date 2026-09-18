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
| macOS 13+ Apple Silicon | 6.1.1 / 6.1.2 | [Beta 2 DMG](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-2/Bitwig-Superpowers-macOS-AppleSilicon-Beta-2.dmg) |
| Windows 10/11 x64 | 6.1.1 | [Beta 2 EXE](https://github.com/kalifrn6-art/bitwig-superpowers/releases/download/superpowers-beta-2/Bitwig-Superpowers-Windows-x64-Beta-2.exe) |

The Mac installer detects the installed version and selects a reviewed profile.
Beta 2 includes the corrected Audio Tools entry point and bundled media tools;
analysis and patching implementations remain compiled.
Unknown future versions are not supported automatically. Read the release-specific
testing limitations before installing. The Mac beta is ad-hoc signed, not
Developer ID signed or notarized.

These beta installers are version-specific. They deliberately stop on an unknown
or modified Bitwig JAR instead of guessing. Support for a new Bitwig release is
published only after its detected profile and resulting patch have been reviewed
and tested.

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
helps me keep building new tools and improving them. Support is always optional.
[Buy Me a Coffee](https://buymeacoffee.com/kalifrn)

Use beta software on backed-up projects. Nothing is uploaded automatically. To
report a problem, open a GitHub issue with your operating system, exact Bitwig
version, installer version, steps to reproduce, and sanitized logs. Never upload
your Bitwig JAR, license data, private projects, credentials, or personal paths.

Bitwig Studio is a product of Bitwig GmbH. This project is independent and is not
affiliated with or endorsed by Bitwig GmbH.
