# Bitwig Superpowers

Native MIDI Tools and Audio Tools for Bitwig Studio.

This repository is the public download page. The implementation and development
history are private. Installers do not include Bitwig Studio, Bitwig vendor JARs,
license keys, or a Bitwig license. You must use your own valid Bitwig installation
and license.

## Downloads

Replacement installer packages are being prepared. There are currently no public
installer releases on this new download page. Older script-based packages were
not copied here because they include implementation source.

When available, download installers only from the [Releases](https://github.com/kalifrn6-art/bitwig-superpowers/releases)
page. Do not use GitHub's automatically generated “Source code” archives; they
contain only this public download-page README.

### Previous beta compatibility (not currently available here)

| Platform | Supported Bitwig version | Package |
|---|---:|---|
| macOS Apple Silicon | 6.1.1 | Bitwig Superpowers Beta 1 |
| Windows x64 | 6.1.1 | Bitwig Superpowers Windows Beta 1.1 |

These beta installers are version-specific. They deliberately stop on an unknown
or modified Bitwig JAR instead of guessing. Support for a new Bitwig release is
published only after its detected profile and resulting patch have been reviewed
and tested.

## Before installing

Save your projects and fully quit Bitwig Studio, its audio engine, and plug-in
hosts. Keep the complete extracted installer folder because it contains the
restore tools. The installer verifies the target and creates a verified backup
before replacing anything.

The Windows Audio Tools runtime requires official Python 3.11 x64, FFmpeg/ffprobe,
and the Microsoft Visual C++ x64 runtime. Optional dependencies and models may
require outbound HTTPS during setup. No inbound firewall rule is required.

## Safety and support

Use beta software on backed-up projects. Nothing is uploaded automatically. To
report a problem, open a GitHub issue with your operating system, exact Bitwig
version, installer version, steps to reproduce, and sanitized logs. Never upload
your Bitwig JAR, license data, private projects, credentials, or personal paths.

Bitwig Studio is a product of Bitwig GmbH. This project is independent and is not
affiliated with or endorsed by Bitwig GmbH.
