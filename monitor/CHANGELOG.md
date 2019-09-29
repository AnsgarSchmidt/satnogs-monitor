# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]
### Added
- 

### Changed
- Display as many future jobs as possible.
- Compiles on stable Rust.

### Fixed
- Typos
- Defaults for non essential config file entries.
- Background of the log window is cleared on display.

## [0.1.1] - 2018-11-18
### Added
- Command line parameter -o|--orbit which specifies how many orbits of the
  current satellite are plotted on the map.
 
### Changed
- Reduced SatNOGS API calls.
- Reduced CPU load and update satellite ground tracks only when orbit number
  has changed.
- Reduced used colors to base16 until themes have landed (to support hopefully
  all terminal emulators).

### Fixed
- Fix parse error when the station hasn't been seen by the network.
