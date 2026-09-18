# Bitwig Superpowers

Native MIDI Tools and Audio Tools for Bitwig Studio.

This repository is the public download page. The implementation and development
history are private. Installers do not include Bitwig Studio, Bitwig vendor JARs,
license keys, or a Bitwig license. You must use your own valid Bitwig installation
and license.

## Downloads

The macOS download is a native graphical installer in a DMG, with its own Python
and FFmpeg/ffprobe. No command launcher or separate Python installation is needed.
Windows currently uses a compiled-runtime command package; a native EXE is pending.
Readable project implementation source is not distributed. Compiled code can
still be reverse-engineered.

Download installers only from the [Releases](https://github.com/kalifrn6-art/bitwig-superpowers/releases)
page. Do not use GitHub's automatically generated “Source code” archives; they
contain only this public download-page README.

### Current beta compatibility

| Platform | Supported Bitwig version | Package |
|---|---:|---|
| macOS 13+ Apple Silicon | 6.1.1 / 6.1.2 | [Mac native installer Beta 1](https://github.com/kalifrn6-art/bitwig-superpowers/releases/tag/superpowers-macos-installer-beta1) |
| Windows x64 | 6.1.1 | [Windows compiled Beta 1.2](https://github.com/kalifrn6-art/bitwig-superpowers/releases/tag/superpowers-windows-beta1.2-compiled) |

The Mac installer detects the installed version and selects a reviewed profile.
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

The Windows Audio Tools runtime requires official Python 3.11 x64, FFmpeg/ffprobe,
and the Microsoft Visual C++ x64 runtime. Optional dependencies and models may
require outbound HTTPS during setup. No inbound firewall rule is required.

## Safety and support

If these tools help your music, consider supporting the project. Your support
helps me keep building new tools and improving them. Support is always optional.

Use beta software on backed-up projects. Nothing is uploaded automatically. To
report a problem, open a GitHub issue with your operating system, exact Bitwig
version, installer version, steps to reproduce, and sanitized logs. Never upload
your Bitwig JAR, license data, private projects, credentials, or personal paths.

Bitwig Studio is a product of Bitwig GmbH. This project is independent and is not
affiliated with or endorsed by Bitwig GmbH.
