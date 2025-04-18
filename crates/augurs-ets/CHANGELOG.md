# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.8.1](https://github.com/grafana/augurs/compare/augurs-ets-v0.8.0...augurs-ets-v0.8.1) - 2025-01-07

### Other

- update Cargo.toml dependencies

## [0.7.0](https://github.com/grafana/augurs/compare/augurs-ets-v0.6.3...augurs-ets-v0.7.0) - 2024-11-25

### Other

- update Cargo.toml dependencies

## [0.6.3](https://github.com/grafana/augurs/compare/augurs-ets-v0.6.2...augurs-ets-v0.6.3) - 2024-11-20

### Other

- update Cargo.toml dependencies

## [0.5.2](https://github.com/grafana/augurs/compare/augurs-ets-v0.5.1...augurs-ets-v0.5.2) - 2024-10-25

### Other

- add benchmark for Prophet ([#140](https://github.com/grafana/augurs/pull/140))

## [0.5.1](https://github.com/grafana/augurs/compare/augurs-ets-v0.5.0...augurs-ets-v0.5.1) - 2024-10-24

### Other

- define lints in Cargo.toml instead of each crate's lib.rs ([#138](https://github.com/grafana/augurs/pull/138))

## [0.5.0](https://github.com/grafana/augurs/compare/augurs-ets-v0.5.0...augurs-ets-v0.4.3) - 2024-10-18

No changes to the Rust crate; this version bump is due to breaking changes in the
Javascript package.

## [0.4.0](https://github.com/grafana/augurs/compare/augurs-ets-v0.3.1...augurs-ets-v0.4.0) - 2024-10-16

### Added

- add 'augurs' convenience crate, re-exporting other crates ([#117](https://github.com/grafana/augurs/pull/117))

### Other

- Add Prophet algorithm in `augurs-prophet` crate ([#118](https://github.com/grafana/augurs/pull/118))

## [0.3.1](https://github.com/grafana/augurs/compare/augurs-ets-v0.3.0...augurs-ets-v0.3.1) - 2024-07-30

No notable changes in this release.

## [0.3.0](https://github.com/grafana/augurs/compare/augurs-ets-v0.2.0...augurs-ets-v0.3.0) - 2024-07-30

### Other
- Add MAD outlier algorithm ([#89](https://github.com/grafana/augurs/pull/89))
- Update nalgebra requirement from 0.32.2 to 0.33.0 ([#93](https://github.com/grafana/augurs/pull/93))
- Remove unsupported .github/workflows/bencher subdirectory and old benchmark workflow ([#90](https://github.com/grafana/augurs/pull/90))

## [0.2.0](https://github.com/grafana/augurs/compare/augurs-ets-v0.1.2...augurs-ets-v0.2.0) - 2024-06-05

### Added
- [**breaking**] add transformations and high-level forecasting API ([#65](https://github.com/grafana/augurs/pull/65))

### Other
- Silence nightly clippy warning
- use clone_from instead of assigning result of clone ([#73](https://github.com/grafana/augurs/pull/73))

## [0.1.1](https://github.com/grafana/augurs/compare/augurs-ets-v0.1.0...augurs-ets-v0.1.1) - 2024-02-15

### Other
- fix clippy lint for unneeded vec macro ([#53](https://github.com/grafana/augurs/pull/53))
- Add license files to repo root and symlinks in crate directories ([#43](https://github.com/grafana/augurs/pull/43))
- Add repository to sub-crate Cargo.tomls ([#42](https://github.com/grafana/augurs/pull/42))

## [0.1.0-alpha.0](https://github.com/grafana/augurs/releases/tag/augurs-ets-v0.1.0-alpha.0) - 2023-09-08

### Other
- Add workspace metadata and use in all the subpackages ([#33](https://github.com/grafana/augurs/pull/33))
- (cargo-release) version 0.1.0-alpha.1
- Use -alpha.0 suffix in crate versions
- Add some more comments and debug assertions
- Update some comments
- Bump all versions to latest ([#26](https://github.com/grafana/augurs/pull/26))
- Update itertools requirement from 0.10.5 to 0.11.0 ([#25](https://github.com/grafana/augurs/pull/25))
- Only bother calculating AMSE when it's required ([#24](https://github.com/grafana/augurs/pull/24))
- Make slight changes to inner loop to avoid as much unsafe indexing ([#23](https://github.com/grafana/augurs/pull/23))
- Add __repr__ for pyaugurs structs
- Add iai benchmarks for benchmarking in CI ([#9](https://github.com/grafana/augurs/pull/9))
- Use workspace dependencies for some more shared dependencies
- Don't hardcode 95% CI ppf in NaiveTrend prediction intervals
- Modify compute_sigma_h to be more functional
- Short circuit where horizon == 0 in predict methods
- Initial commit
