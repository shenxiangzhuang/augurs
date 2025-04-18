# augurs - a time series toolkit for Rust

[![Python](https://github.com/grafana/augurs/actions/workflows/python.yml/badge.svg)](https://github.com/grafana/augurs/actions/workflows/python.yml)
[![Rust](https://github.com/grafana/augurs/actions/workflows/rust.yml/badge.svg)](https://github.com/grafana/augurs/actions/workflows/rust.yml)
[![docs.rs](https://docs.rs/augurs-core/badge.svg)](https://docs.rs/augurs-core)
[![crates.io](https://img.shields.io/crates/v/augurs-core.svg)](https://crates.io/crates/augurs-core)

This repository contains `augurs`, a time series toolkit built in Rust.
It aims to provide some useful primitives for working with time series,
as well as the main functionality: heavily optimized models for forecasting,
outlier detection, clustering, seasonality detection, changepoint detection
and more. Most algorithms are based on existing R or Python implementations.

As well as the core Rust library, augurs will provide bindings to other
languages such as Python and Javascript (via WASM).

[Check out the demo][demo] to see what augurs can do!

> [!IMPORTANT]
> Please note that this is not an official Grafana project, so
> maintenance may be a bit slower than usual. It's still early days too
> so expect some rough edges and changes to APIs!

## Crate descriptions

| Name                     | Purpose                                                                      |
| ------------------------ | ---------------------------------------------------------------------------- |
| [`augurs`]               | Wrapper crate exposing functionality of all main crates behind feature flags |
| [`augurs-changepoint`][] | Changepoint detection for time series                                        |
| [`augurs-clustering`][]  | Time series clustering algorithms                                            |
| [`augurs-core`][]        | Common structs and traits                                                    |
| [`augurs-dtw`][]         | Dynamic Time Warping (DTW)                                                   |
| [`augurs-ets`][]         | Automatic exponential smoothing models                                       |
| [`augurs-mstl`][]        | Multiple Seasonal Trend Decomposition using LOESS (MSTL)                     |
| [`augurs-outlier`][]     | Outlier detection for time series                                            |
| [`augurs-prophet`][]     | The Prophet time series forecasting algorithm                                |
| [`augurs-seasons`][]     | Seasonality detection using periodograms                                     |
| [`augurs-testing`][]     | Testing data and, eventually, evaluation harness for implementations         |
| [`js/*`][js-libs]        | WASM bindings to augurs                                                      |
| [`pyaugurs`][]           | Python bindings to augurs                                                    |

## Developing

This project uses [`just`] as a command runner; this will need to be installed separately.
See the [`justfile`](./justfile) for more information.

Some of the tasks require [`bacon`], which will also need to be installed separately.

## Releasing

Releases are made using `release-plz`: a PR should be automatically created for each release, and merging will perform the release and publish automatically.

### Releasing the `augurs` Python library

The first exception to the `release-plz` flow is the `augurs` Python library, which is only released when a new tag beginning with `pyaugurs` is pushed. This must be done manually for now (ideally soon after the `release-plz` PR is merged).

E.g.:

```bash
git tag pyaugurs-v0.3.0 -m "Release pyaugurs v0.3.0"
git push --tags
```

### Releasing the `augurs` npm library

The `augurs` npm library must also be published manually. This can be done using `just publish-augurs-js`; note you'll need to login with npm first.

```bash
npm login
# Log in online, etc...
just publish-augurs-js
```

## License

Dual-licensed to be compatible with the Rust project.
Licensed under the Apache License, Version 2.0 `<http://www.apache.org/licenses/LICENSE-2.0>` or the MIT license `<http://opensource.org/licenses/MIT>`, at your option.

[`augurs`]: https://crates.io/crates/augurs
[`augurs-changepoint`]: https://crates.io/crates/augurs-changepoint
[`augurs-clustering`]: https://crates.io/crates/augurs-clustering
[`augurs-core`]: https://crates.io/crates/augurs-core
[`augurs-dtw`]: https://crates.io/crates/augurs-dtw
[`augurs-ets`]: https://crates.io/crates/augurs-ets
[`augurs-mstl`]: https://crates.io/crates/augurs-mstl
[`augurs-outlier`]: https://crates.io/crates/augurs-outlier
[`augurs-prophet`]: https://crates.io/crates/augurs-prophet
[`augurs-seasons`]: https://crates.io/crates/augurs-seasons
[`augurs-testing`]: https://crates.io/crates/augurs-testing
[js-libs]: https://github.com/grafana/augurs/tree/main/js
[`pyaugurs`]: https://crates.io/crates/pyaugurs
[`just`]: https://just.systems/man/en/
[`bacon`]: https://dystroy.org/bacon
[demo]: https://demo.augu.rs
