# Ra — Free Windows Gamma Control

**See more in the dark.** Adjust Windows SDR gamma from the system tray. Switch between Gamma 1.3, Gamma 1.5, your own Custom curve and Neutral.

**[Download Ra 0.4.2 for Windows — Installer (.exe)](https://github.com/sobrilo8/ra-releases/releases/download/v0.4.2-net10-preview.1/Ra-Setup-v0.4.2-net10-preview.1-win-x64.exe)**

[Portable ZIP](https://github.com/sobrilo8/ra-releases/releases/download/v0.4.2-net10-preview.1/Ra-v0.4.2-net10-preview.1-portable-win-x64.zip) · [Release notes & SHA-256 checksums](https://github.com/sobrilo8/ra-releases/releases/tag/v0.4.2-net10-preview.1) · [Send feedback](https://forms.gle/rtTrEG4AJ5EmLFn5A)

**Free · Windows 10/11 x64 · Version 0.4.2**  
**Note:** Ra is currently an unsigned preview release. Windows may display a security warning because the application does not yet have a digital signing certificate. Only install software from sources you trust.

![Ra gamma controls — product illustration](assets/ra-github-banner.png)

## What Ra does

- **Quick presets:** Switch between Gamma 1.3, Gamma 1.5 and Neutral from the tray.
- **Custom curve:** Drag points to preview a curve; Save, Reset or cancel your changes.
- **One-click toggle:** Left-click the tray icon to switch between Neutral and your last active profile.
- **Optional update checks:** Check manually or opt in to checks no more than once per 24 hours. Automatic checks are off by default; Ra never downloads or installs updates silently.
- **No accounts or tracking:** No account, advertisements or telemetry. Display settings stay on your PC. See [Privacy](PRIVACY.md) for GitHub update checks and optional Google Forms feedback.

## Install in three steps

1. **Download the installer** using the link above. The [portable ZIP](https://github.com/sobrilo8/ra-releases/releases/download/v0.4.2-net10-preview.1/Ra-v0.4.2-net10-preview.1-portable-win-x64.zip) is an alternative if you prefer extracting the files yourself.
2. **If you're updating Ra**, quit the running app using **Settings → Quit Ra** first. Then run the installer. It normally installs for your Windows user into `%LOCALAPPDATA%\Programs\Ra`.
3. **Use Ra from the system tray.** If the icon is hidden, expand the tray's hidden icons. Right-click to select a preset or open Settings; left-click to toggle Neutral and your last non-neutral profile.

The self-contained download does not need a separate .NET installation. An optional **Start with Windows** setting is available.

## Compatibility and limitations

Ra adjusts the Windows **GDI gamma ramp**. It is not a monitor calibration tool and does not measure physical brightness or color accuracy. Some drivers, games and display modes may override gamma changes. HDR, ICC, fullscreen-game, anti-cheat and multi-monitor behavior have not been comprehensively tested.

On Neutral or normal Quit, Ra attempts to restore the preceding gamma ramp **only if it still owns its last verified change**. Crashes or forced termination can prevent restoration.

<details>
<summary><strong>Technical details and file storage</strong></summary>

- Target: Windows 10/11 x64; C# WinForms, self-contained .NET 10.
- The installer and portable ZIP are available in the [0.4.2 release](https://github.com/sobrilo8/ra-releases/releases/tag/v0.4.2-net10-preview.1), each with a corresponding `.sha256` checksum file.
- Gamma profile data is stored in `%LOCALAPPDATA%\Ra\state.txt`; optional automatic-update preferences in `%LOCALAPPDATA%\Ra\updates.txt`. Even the portable version writes local preferences.
- Custom control-point coordinates are saved to four decimal places, so restored numeric values may differ slightly from full-precision previews. The visual impact has not been measured.
- The public repository contains documentation and downloadable binaries, **not the private development source history**.

</details>

## Help, privacy and security

- [What changed in 0.4.2](CHANGELOG.md)
- [Privacy and network activity](PRIVACY.md)
- [Private vulnerability reporting](SECURITY.md)
- [Send feedback](https://forms.gle/rtTrEG4AJ5EmLFn5A)

## License

Ra is distributed under the [MIT license](LICENSE), with the existing Ra contributor and Vaster copyright notices. Distribution archives include the applicable license and notice files for bundled Microsoft .NET components.
