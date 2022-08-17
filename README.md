# RabbitMQ Snap for arm64

[![rabbitmq-server-snap](https://snapcraft.io/rabbitmq-server-snap/badge.svg)](https://snapcraft.io/rabbitmq-server-snap)
[![rabbitmq-server-snap](https://snapcraft.io/rabbitmq-server-snap/trending.svg?name=0)](https://snapcraft.io/rabbitmq-server-snap)
[![CI](https://github.com/ML-PA-Consulting-GmbH/rabbitmq-server-snap/actions/workflows/CI.yaml/badge.svg)](https://github.com/ML-PA-Consulting-GmbH/rabbitmq-server-snap/actions/workflows/CI.yaml)
![GitHub issues](https://img.shields.io/github/issues/ML-PA-Consulting-GmbH/rabbitmq-server-snap)
![GitHub pull requests](https://img.shields.io/github/issues-pr/ML-PA-Consulting-GmbH/rabbitmq-server-snap)

Snapped version of RabbitMQ for **arm64** and **amd64**.

It's based on up to date versions of RabbitMQ, Elixir and Erlang (as of 2022-08-16)

The snap package is still in **alpha**, don't use for production, yet.

## Notes on snap building process

Both snaps (arm64, amd64) are built from precompiled binaries. Snapcraft currently doesn't offer any usable method
for building arm64 snaps on a amd64 machine as cross-compiling is discouraged and building using an arm-VM is not possible in CI/CD.
Therefor binaries seem to be the only sensible choice. 

As snapcraft can't check dependencies of arm64 libraries when building on amd64, a lot of warnings are produced during the process.

The amd64 build process is designed strictly analog to the arm64 build process to check that dependencies are fulfilled. 

The `libwxgtk3` branch of dependencies is not included, as it takes a lot of storage space and is not needed for running a background service 
like rabbitmq. Warnings about this library missing can therefore be ignored.

**Attention:** While the amd64 version is checked after every build, the arm64 version is not - as no arm64 device is available for testing
in the CI/CD pipeline.

## Notes on publishing a new release

To publish a new release, add a new version in CHANGELOG.md - this will trigger the release process.

## Credits

Based on: 
- https://github.com/rabbitmq/rabbitmq-server
- https://github.com/elixir-lang/elixir
- https://github.com/erlang/otp
- https://github.com/nicolasbock/rabbitmq-server-snap
