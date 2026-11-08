# Security policy — Ra

## Supported releases

The latest **published** Windows preview, if any, is the only release targeted for maintenance. There is currently no promise of long-term support for any early preview or test build.

## Report a vulnerability privately

**Before public distribution, the repository maintainer must enable GitHub private vulnerability reporting** under the repository's security settings.

Once enabled, use the repository's **Security → Report a vulnerability** flow. Do not disclose exploit details, private data or proofs of concept in public Issues.

If this option is not visible, do not assume that posting a public issue is a confidential report. Contact the maintainer through a separately verified private channel.

## Scope

Ra is a local Windows system-tray program with no built-in accounts, telemetry or internet updater. It reads/writes Windows display gamma ramps, maintains local preferences and can optionally configure a current-user startup registry entry. It does not claim protection against untrusted local processes or display-driver faults.
