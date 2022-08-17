# Changelog

Version names are built from the contained RabbitMQ version (3.X.X) and
the revision of the snap package, resulting in a version number like e.g. 3.10.7-42
_

## [3.10.7-6] - 2022-08-17

Testing conditional release in github workflow

- Update: release is only performed, if new version is found in CHANGELOG.md

## [3.10.7-1] - 2022-08-17

Optimizing the build pipeline

- Update: changed naming scheme for versions to <RabbitMQ-version>-<SnapPackageRevision> e.g. 3.10.7-1

## [3.10.7-0] - 2022-08-17

Developing build and release pipeline. Version not usable, yet.

- Fix: automatically install snap and read version from `snap info`
