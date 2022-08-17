# Changelog

Version names are built from the contained RabbitMQ version (3.X.X) and
the revision of the snap package, resulting in a version number like e.g. 3.10.7-42

## [3.10.7-014] - 2022-08-17

- Update: releases are now automatically published from CI/CD when pushing CHANGELOG.md with new version number

## [3.10.7-008] - 2022-08-17

All tests run successful for amd64 build. 

- Fix: environmental variables in run scripts
- Fix: various fixes in snapcraft.yaml 
_

## [3.10.7-007] - 2022-08-17

Github workflow is building arm64 and arm64, testing amd64 and publishing new releases

- Update: release is only performed, if new version is found in CHANGELOG.md

## [3.10.7-000] - 2022-08-17

Developing build and release pipeline. Version not usable, yet.

- Fix: automatically install snap and read version from `snap info`
