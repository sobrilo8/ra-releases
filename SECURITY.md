# Security policy — Ra

## Supported releases

The latest **published** Windows preview is the only release currently targeted for maintenance. No long-term support commitment is made for early preview builds.

## Report a vulnerability privately

**Private vulnerability reporting is enabled** for this repository. Use **Security → Report a vulnerability** on the [Ra GitHub repository](https://github.com/sobrilo8/ra-releases) to submit a confidential report.

Please do not post exploit details, secrets, private information or proofs of concept in public Issues. If the private reporting option is unavailable, do not assume a public Issue is confidential; seek a separately verified private contact route.

## Scope

Ra is a Windows tray utility that reads and writes GDI gamma ramps and stores local preferences. It contains no accounts, telemetry or silent installer updater. Version 0.4.2 performs manual or opt-in GitHub release-metadata checks and opens a Google Forms feedback page only after a click.

The unsigned preview is not guaranteed to work with every GPU driver, fullscreen game, anti-cheat configuration, HDR mode or multi-monitor setup. Ra makes no claim of protection against untrusted local processes or display-driver faults.
