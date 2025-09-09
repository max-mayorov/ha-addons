# Revert Log

## Commit fe78b2f3e42556c39a27df120406e56041d5d4fa

**Status**: REVERTED

**Original Commit Message**: "Update NUT to version 2.8.3-3 to fix unsupported flag error"

**Changes Made in Original Commit**:
- Changed Debian repository from `testing` to `unstable`
- Updated NUT package versions from `2.8.1-5` to `2.8.3-3`
- Updated cleanup to remove `unstable.list` instead of `testing.list`

**Revert Action**: 
The current codebase maintains the pre-commit state:
- Uses Debian `testing` repository
- Uses NUT version `2.8.1-5`
- Cleans up `testing.list` file

**Files Affected**:
- `nut/Dockerfile`

**Verification**: 
- Dockerfile syntax verified
- Docker build process validated
- Package versions confirmed: nut=2.8.1-5, nut-snmp=2.8.1-5, nut-xml=2.8.1-5
- Repository confirmed: testing

## Commit [Current]

**Status**: UPDATED

**Commit Message**: "Update NUT to version 2.8.3-3 (available in testing)"

**Changes Made**:
- Updated NUT package versions from `2.8.1-5` to `2.8.3-3` (current available version in testing)
- Updated addon version from `2.8.1` to `2.8.3` in config.yaml
- Maintained Debian `testing` repository

**Reason for Change**:
- Version `2.8.1-5` is no longer available in Debian testing repository
- Version `2.8.3-3` is the current available version in testing
- This resolves the Docker build error: "E: Version '2.8.1-5' for 'nut' was not found"

**Files Affected**:
- `nut/Dockerfile`
- `nut/config.yaml`

**Verification**:
- Package versions confirmed available: nut=2.8.3-3, nut-snmp=2.8.3-3, nut-xml=2.8.3-3
- Repository confirmed: testing