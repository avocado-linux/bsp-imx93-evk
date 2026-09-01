# Changelog

All notable changes to avocado-bsp-imx93-evk are documented in this file.
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.1.1]

### Fixed
- `ext install` no longer fails on the 2026 feed. `kernel-module-crct10dif-ce`
  and `kernel-module-rtc-pcf2131` exist only in the downstream 6.6 kernel, so
  they are now scoped with `kernel-6.6.*` rather than requested
  unconditionally. On 6.18 the CRC acceleration is built in and the PCF2131 is
  handled by `rtc-pcf2127`.

## [0.1.0]

### Added
- Initial release: Board support for the i.MX 93 EVK.
- CI via the shared `avocado-linux/actions` reusable workflows: PR build check
  (`test.yml`) and tag-driven package + publish to the Avocado feed (`release.yml`).
