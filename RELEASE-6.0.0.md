# Superpowers Beta 6.0.0 — Bitwig 6.1.7

New and updated native workflows, alongside the tools from Beta 5.0.2.

## New

- MIDI Comp: build a performance from sections of MIDI takes and keep editing the notes.
- Glissando in MIDI Tools, plus updated visual helpers for Stacks, Strum and Glissando.
- Browser Rank and sorting for finding frequently used items.
- Clean Waveforms with improved waveform detail when zooming.
- Settings → Mods to choose which Superpowers features to use.

## Updated

- Freeze keeps the MIDI-note representation, snowflake indicator and hatched tails. Queue handling stops transport before renders, allows plug-ins to settle and checks engine recovery after the queue.
- Capture MIDI supports adding captured notes to an existing clip while playing. Separate clips retain their existing behavior; merge them manually when needed.
- Updated for the separately built macOS, Windows and Linux versions of Bitwig 6.1.7.

Export with FX, Ramp, the existing MIDI and Audio Tools, Detect Event Key, piano-roll editing improvements, group tools and device shortcuts remain included. The retired Cmd+3 straight/triplet toggle remains removed.

## Compatibility and validation

**This release supports exactly Bitwig Studio 6.1.7.** macOS 13+ Apple Silicon, Windows 10/11 x64, or Linux x64. Installers require your own valid Bitwig installation and license; they do not include Bitwig Studio or vendor JARs.

macOS Freeze and Capture behavior has been confirmed by the user. All three installers passed payload checksum verification, exact reconstruction of their candidate, bytecode/reference checks and verification that the modified-JAR integrity check is disabled. Windows started in an isolated CrossOver test; this is not native Windows validation. **Windows and Linux interactive validation is pending.** Offline checks do not prove every project, plug-in or workflow. Optional Audio Tools require their runtime; Linux Audio Tools setup remains pending.

Save and back up projects, then fully quit Bitwig and its engine before installing. The installer verifies the exact input and preserves a backup. Use Restore Original to revert, or Send Report for a sanitized support bundle. macOS is ad-hoc signed, not notarized; the Windows EXE is not code-signed.

## Superpowers for Patchbay (beta 6.0.0-dev.2)

Platform bundles (`Superpowers-Patchbay-6.0.0-dev.2-{macos,windows,linux}.zip`) are included for unmodified **Bitwig Studio 6.1.7** with **Patchbay 0.36.0-dev.16**. Each outer ZIP contains 21 Superpowers mods and 3 required frameworks (22 selected functions; Clean Waveforms is excluded).

1. Extract the outer platform ZIP, leaving the 24 ZIPs inside `mods/` compressed.
2. In Patchbay, select your unmodified Bitwig 6.1.7 installation under Settings, then use **Mods → Add Mod…** to import all 24 ZIPs for your operating system. Do not mix platform ZIP sets.
3. Enable the desired mods and click Load.

The macOS source selection was tested by the author; symbol-map cleanup and the experimental Windows and Linux bundles passed offline preparation, reflection/direct-reference verification, and real Patchbay launcher import/update/digest-rejection checks. **Windows and Linux Patchbay bundles are experimental and have not been tested interactively on those operating systems.**

### Patchbay Launcher catalog

All 24 inner ZIPs per platform are also published as individual release assets: 21 Superpowers mods and the 3 required frameworks (72 ZIPs total). Add a **Mods** source for repository `kalifrn6-art/bitwig-superpowers` and use the filter for your operating system:

| Platform | Source filter |
|---|---|
| macOS | `*.macos.zip` |
| Windows (experimental) | `*.windows.zip` |
| Linux (experimental) | `*.linux.zip` |

Assets use `<mod-id>-<version>.<platform>.zip`, for example `superpowers-freeze-6.0.0-dev.2.macos.zip`. The stable preferences framework uses `preferences-composition-framework-1.0.0-platform.macos.zip` (or `.windows.zip` / `.linux.zip`) so the Launcher accepts the filename. ZIP contents and manifest versions are unchanged from the bundles. Include all three frameworks: **Actions and Menus**, **Inspector**, and **Preferences**; these existing packages do not declare all framework dependencies in the Launcher's `requires` field, so select the frameworks explicitly. Use only one platform filter. The original bundles remain available for manual import.

For Bitwig 6.1.5, keep Beta 5.0.2; for 6.1.3/6.1.4, keep Beta 5. These installers are not an automatic compatibility promise for later Bitwig versions.

[Feature tour and downloads](https://kalifrn.com/superpowers/) · [Support Superpowers](https://buy.stripe.com/9B64gA1b04jzaJbgyi1Jm00)

SHA-256 checksums are attached in SHA256SUMS-6.0.0.txt.

### Individual Patchbay mod assets

| Mod | Release asset | Platform |
|---|---|---|
| Framework: Actions and Menus | `action-menu-composition-framework-0.8.0-dev.1.macos.zip` | macos |
| Framework: Inspector | `inspector-composition-framework-0.3.0-dev.2.macos.zip` | macos |
| Framework: Settings | `preferences-composition-framework-1.0.0-platform.macos.zip` | macos |
| Arranger: Superpowers Nudge Overlap Recovery | `superpowers-arranger-nudge-6.0.0-dev.2.macos.zip` | macos |
| Superpowers: Audio Tools | `superpowers-audio-tools-6.0.0-dev.2.macos.zip` | macos |
| Superpowers: Browser Rank | `superpowers-browser-rank-6.0.0-dev.2.macos.zip` | macos |
| Superpowers: Browser Sort Memory and Folders | `superpowers-browser-sort-6.0.0-dev.2.macos.zip` | macos |
| Capture MIDI: Superpowers | `superpowers-capture-midi-6.0.0-dev.2.macos.zip` | macos |
| Arranger: Superpowers Comp Fades | `superpowers-comp-fades-6.0.0-dev.2.macos.zip` | macos |
| Superpowers: Continuous Takes | `superpowers-continuous-take-6.0.0-dev.2.macos.zip` | macos |
| Superpowers: Device Shortcuts | `superpowers-device-keys-6.0.0-dev.2.macos.zip` | macos |
| Superpowers: Export with FX | `superpowers-export-fx-6.0.0-dev.2.macos.zip` | macos |
| Arranger: Superpowers Freeze | `superpowers-freeze-6.0.0-dev.2.macos.zip` | macos |
| Superpowers: Group Color | `superpowers-group-color-6.0.0-dev.2.macos.zip` | macos |
| Superpowers: Compact Group Height | `superpowers-group-height-6.0.0-dev.2.macos.zip` | macos |
| Arranger: Superpowers Group Summary Opacity | `superpowers-group-summary-6.0.0-dev.2.macos.zip` | macos |
| Superpowers: MIDI Comping | `superpowers-midi-comp-6.0.0-dev.2.macos.zip` | macos |
| Superpowers: MIDI Tools | `superpowers-midi-tools-6.0.0-dev.2.macos.zip` | macos |
| Superpowers: Piano Roll Keys | `superpowers-piano-roll-keys-6.0.0-dev.2.macos.zip` | macos |
| Superpowers: Plug-in Load Timeout | `superpowers-plugin-load-timeout-6.0.0-dev.2.macos.zip` | macos |
| Piano Roll: Superpowers Velocity Ramp | `superpowers-ramp-velocity-6.0.0-dev.2.macos.zip` | macos |
| Superpowers: Selection Follows Notes | `superpowers-selection-follows-6.0.0-dev.2.macos.zip` | macos |
| Superpowers: Track Shortcuts | `superpowers-track-keys-6.0.0-dev.2.macos.zip` | macos |
| Superpowers: Track Range Across Groups | `superpowers-track-range-6.0.0-dev.2.macos.zip` | macos |
| Framework: Actions and Menus | `action-menu-composition-framework-0.8.0-dev.1.windows.zip` | windows |
| Framework: Inspector | `inspector-composition-framework-0.3.0-dev.2.windows.zip` | windows |
| Framework: Settings | `preferences-composition-framework-1.0.0-platform.windows.zip` | windows |
| Arranger: Superpowers Nudge Overlap Recovery | `superpowers-arranger-nudge-6.0.0-dev.2.windows.zip` | windows |
| Superpowers: Audio Tools | `superpowers-audio-tools-6.0.0-dev.2.windows.zip` | windows |
| Superpowers: Browser Rank | `superpowers-browser-rank-6.0.0-dev.2.windows.zip` | windows |
| Superpowers: Browser Sort Memory and Folders | `superpowers-browser-sort-6.0.0-dev.2.windows.zip` | windows |
| Capture MIDI: Superpowers | `superpowers-capture-midi-6.0.0-dev.2.windows.zip` | windows |
| Arranger: Superpowers Comp Fades | `superpowers-comp-fades-6.0.0-dev.2.windows.zip` | windows |
| Superpowers: Continuous Takes | `superpowers-continuous-take-6.0.0-dev.2.windows.zip` | windows |
| Superpowers: Device Shortcuts | `superpowers-device-keys-6.0.0-dev.2.windows.zip` | windows |
| Superpowers: Export with FX | `superpowers-export-fx-6.0.0-dev.2.windows.zip` | windows |
| Arranger: Superpowers Freeze | `superpowers-freeze-6.0.0-dev.2.windows.zip` | windows |
| Superpowers: Group Color | `superpowers-group-color-6.0.0-dev.2.windows.zip` | windows |
| Superpowers: Compact Group Height | `superpowers-group-height-6.0.0-dev.2.windows.zip` | windows |
| Arranger: Superpowers Group Summary Opacity | `superpowers-group-summary-6.0.0-dev.2.windows.zip` | windows |
| Superpowers: MIDI Comping | `superpowers-midi-comp-6.0.0-dev.2.windows.zip` | windows |
| Superpowers: MIDI Tools | `superpowers-midi-tools-6.0.0-dev.2.windows.zip` | windows |
| Superpowers: Piano Roll Keys | `superpowers-piano-roll-keys-6.0.0-dev.2.windows.zip` | windows |
| Superpowers: Plug-in Load Timeout | `superpowers-plugin-load-timeout-6.0.0-dev.2.windows.zip` | windows |
| Piano Roll: Superpowers Velocity Ramp | `superpowers-ramp-velocity-6.0.0-dev.2.windows.zip` | windows |
| Superpowers: Selection Follows Notes | `superpowers-selection-follows-6.0.0-dev.2.windows.zip` | windows |
| Superpowers: Track Shortcuts | `superpowers-track-keys-6.0.0-dev.2.windows.zip` | windows |
| Superpowers: Track Range Across Groups | `superpowers-track-range-6.0.0-dev.2.windows.zip` | windows |
| Framework: Actions and Menus | `action-menu-composition-framework-0.8.0-dev.1.linux.zip` | linux |
| Framework: Inspector | `inspector-composition-framework-0.3.0-dev.2.linux.zip` | linux |
| Framework: Settings | `preferences-composition-framework-1.0.0-platform.linux.zip` | linux |
| Arranger: Superpowers Nudge Overlap Recovery | `superpowers-arranger-nudge-6.0.0-dev.2.linux.zip` | linux |
| Superpowers: Audio Tools | `superpowers-audio-tools-6.0.0-dev.2.linux.zip` | linux |
| Superpowers: Browser Rank | `superpowers-browser-rank-6.0.0-dev.2.linux.zip` | linux |
| Superpowers: Browser Sort Memory and Folders | `superpowers-browser-sort-6.0.0-dev.2.linux.zip` | linux |
| Capture MIDI: Superpowers | `superpowers-capture-midi-6.0.0-dev.2.linux.zip` | linux |
| Arranger: Superpowers Comp Fades | `superpowers-comp-fades-6.0.0-dev.2.linux.zip` | linux |
| Superpowers: Continuous Takes | `superpowers-continuous-take-6.0.0-dev.2.linux.zip` | linux |
| Superpowers: Device Shortcuts | `superpowers-device-keys-6.0.0-dev.2.linux.zip` | linux |
| Superpowers: Export with FX | `superpowers-export-fx-6.0.0-dev.2.linux.zip` | linux |
| Arranger: Superpowers Freeze | `superpowers-freeze-6.0.0-dev.2.linux.zip` | linux |
| Superpowers: Group Color | `superpowers-group-color-6.0.0-dev.2.linux.zip` | linux |
| Superpowers: Compact Group Height | `superpowers-group-height-6.0.0-dev.2.linux.zip` | linux |
| Arranger: Superpowers Group Summary Opacity | `superpowers-group-summary-6.0.0-dev.2.linux.zip` | linux |
| Superpowers: MIDI Comping | `superpowers-midi-comp-6.0.0-dev.2.linux.zip` | linux |
| Superpowers: MIDI Tools | `superpowers-midi-tools-6.0.0-dev.2.linux.zip` | linux |
| Superpowers: Piano Roll Keys | `superpowers-piano-roll-keys-6.0.0-dev.2.linux.zip` | linux |
| Superpowers: Plug-in Load Timeout | `superpowers-plugin-load-timeout-6.0.0-dev.2.linux.zip` | linux |
| Piano Roll: Superpowers Velocity Ramp | `superpowers-ramp-velocity-6.0.0-dev.2.linux.zip` | linux |
| Superpowers: Selection Follows Notes | `superpowers-selection-follows-6.0.0-dev.2.linux.zip` | linux |
| Superpowers: Track Shortcuts | `superpowers-track-keys-6.0.0-dev.2.linux.zip` | linux |
| Superpowers: Track Range Across Groups | `superpowers-track-range-6.0.0-dev.2.linux.zip` | linux |
