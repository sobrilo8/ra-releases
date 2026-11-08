# Ra — Windows SDR Gamma Utility

**Free Windows utility · Publisher display name: Vaster · Early preview**

Ra is a lightweight Windows system-tray application that adjusts Windows SDR display gamma curves using the Windows GDI gamma-ramp API. It offers Gamma 1.3, Gamma 1.5 and a user-editable Custom curve, with Neutral to stop Ra's adjustment.

**This is a binary-distribution repository.** The development source code and its Git history are not hosted here. The application is distributed under the included MIT license; that license does not require the source repository to be made public.

## Requirements and limitations

- Windows 10 or 11, x64, on a graphics path supporting GDI gamma ramps.
- The downloadable self-contained build does not require a separate .NET installation.
- Display-driver, HDR, ICC/color-management, multi-monitor, fullscreen and anti-cheat compatibility are not broadly tested.
- Ra is not a monitor calibration tool and does not measure actual physical brightness or color accuracy.
- Gamma changes can be overwritten by Windows, drivers or other apps; crashes or forced termination can prevent restoration.

## How to use

- **Gamma 1.3 / 1.5:** choose a preset from the tray menu.
- **Custom:** open Settings, drag points to preview, click Save to persist the curve, or press Escape to cancel unsaved edits.
- **Neutral:** request restoration of the previous ramp when Ra still owns its last verified write.
- **Left-click the tray icon:** toggle Neutral and the last non-neutral profile.
- **Right-click the tray icon:** open presets and Settings.
- **Start with Windows:** optional, off by default during installation.

Custom point coordinates are persisted to four decimal places. A curve reloaded after restarting may therefore differ numerically from the pre-save, full-precision curve. Its visual impact has not been measured.

## Download, integrity, installation

Download an installer and its `.sha256` file from the official **Releases** section once a release has been published. Compare the installer SHA-256 with the published checksum before running it.

Quit any running Ra normally using **Settings → Quit Ra** before installing, updating or uninstalling it. The installer normally installs per user into `%LOCALAPPDATA%\Programs\Ra`; it offers an optional desktop shortcut and post-install launch.

**Unsigned preview:** this release's installer and application are not digitally signed. Windows may display warnings or block execution. Respect Windows security decisions; do not disable security protections.

Saved preferences are local in `%LOCALAPPDATA%\Ra\state.txt` and are normally retained after uninstall. See [PRIVACY.md](PRIVACY.md).

## Support and security

See [SECURITY.md](SECURITY.md) for the private vulnerability-reporting policy. The maintainer must enable GitHub private vulnerability reporting **before** any public release.

## License

Ra is distributed under the [MIT license](LICENSE) with the existing Ra contributors and Vaster copyright notices. The installer contains applicable license and third-party notice files for bundled Microsoft .NET components.
