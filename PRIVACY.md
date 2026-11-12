# Privacy — Ra 0.4.2 preview

Ra is a Windows system-tray utility for adjusting SDR gamma curves. Ra does not include user accounts, advertising, analytics/telemetry, usage reports or a background installer downloader.

## Local data

Display preferences and a saved Custom curve are stored in:
`%LOCALAPPDATA%\Ra\state.txt`.

Automatic update checking is **off by default**. If enabled, a separate local `%LOCALAPPDATA%\Ra\updates.txt` file stores an enabled flag and the timestamp of the last automatic check attempt. This limits automatic requests to no more than once every 24 hours.

The optional **Start with Windows** setting writes the executable's path to the current user's Windows Run registry entry. Switching it off removes the entry. Exiting Ra alone does not delete the startup setting.

Ra reads and writes Windows GDI gamma ramps to perform its function. It does not upload gamma curves, profiles, machine IDs, logs, screenshots, gameplay information or application usage.

## External network activity

- **Check for updates** contacts GitHub's public release-metadata API only after the user clicks the button, or while automatic checking is explicitly enabled. GitHub receives ordinary HTTP and network information such as the public IP address and a Ra update-checker User-Agent. Ra does not silently download or install releases.
- **View release** opens a GitHub release page in the user's browser only after a click.
- **Send feedback** opens an external Google Forms respondent page only after a click: https://forms.gle/rtTrEG4AJ5EmLFn5A. Ra does not fill in or submit the form. The user chooses what to enter; a contact email address is optional. Google processes form submissions and ordinary browser/network information under its own policies.

No promise of anonymity from GitHub or Google is made. Do not enter passwords or sensitive personal information in feedback.

## Retention and removal

Local display state remains until changed or deleted. Quit Ra normally before deleting `state.txt`. Quit Ra before deleting `updates.txt`; removing that file disables automatic checks for the next start. Disable **Start with Windows** before uninstalling if you do not want the startup entry retained.

Feedback is managed in Google Forms by the form owner, separately from Ra's local application data. Ra cannot delete submitted Google Forms responses.

This document covers Ra 0.4.2 application behavior, not all data collection by Windows, GitHub, Google, network providers or the installer platform.
