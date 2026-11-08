# Privacy — Ra 0.4.1

Ra is a local Windows tray utility. Based on the current application source, Ra does **not** provide an application network client, user accounts, analytics/telemetry, advertising, an updater, or a cloud service.

## Local information

Ra stores its own display preferences at:

```text
%LOCALAPPDATA%\Ra\state.txt
```

This state includes the currently selected profile, most recently selected non-neutral profile, and the user-defined Custom curve. Older versions' `Highlights -10` data can be migrated to a Custom curve; `Highlights -10` is no longer a separate active setting.

When **Start with Windows** is enabled, Ra also uses the current user's Windows Run registry entry:

```text
HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run
Value: Ra
```

The entry contains the local Ra executable path. Disabling the toggle removes the entry; exiting Ra alone does not remove it.

Ra reads and requests changes to the Windows display gamma ramp to perform its function. This is a display setting, not a data upload.

## Retention and deletion

Ra stores these settings locally until they are changed or removed. There is no in-app cloud account or remote data deletion service.

To remove the saved preferences, Quit Ra and delete `%LOCALAPPDATA%\Ra\state.txt`. If Windows startup was enabled, disable it first through Ra Settings or remove the per-user `Ra` Run entry.

This description covers Ra's application functionality, **not** data collection or security features of Windows itself, the download host, or an external distribution platform.
