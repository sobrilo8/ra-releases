# Changelog

## 0.4.2 .NET 10 preview

- Added **About / Updates** with manual update checks against public GitHub releases.
- Optional automatic release checks are disabled by default and limited to at most once per 24 hours; Ra never silently downloads or installs updates.
- Quiet update-available indication without gameplay interruption.
- **Send feedback** opens the external Ra Google Form; email contact is voluntary.
- Improved the panel layout and taskbar clearance.
- Preserved local gamma settings and conservative restoration behavior.

**Validation:** installed 0.4.1 → 0.4.2 upgrade passed the owner's guarded Windows test; the packaged 0.4.2 app was also launched and checked. Clean-machine installation, uninstall and broad hardware compatibility remain unverified. Unsigned binaries.


## 0.4.1 .NET 10 preview

- Self-contained Windows x64 preview using .NET 10.
- Gamma 1.3 and Gamma 1.5 presets, plus editable Custom curve.
- Live Custom preview, Save, Reset and cancel.
- Conditional restoration of the preceding Windows GDI gamma ramp on Neutral/normal Quit.
- Local persistence of profiles and Custom control points.
- Current-user Inno Setup distribution with optional launch and desktop shortcut.

**Known limitations:** limited testing on one Windows x64 machine, four-decimal stored Custom precision, incomplete HDR/ICC/multi-monitor/fullscreen validation, conditional gamma restoration and unsigned binaries. See the release notes distributed with the candidate.

This repository is intended for binary releases only. It does not contain the private development source or its history.
