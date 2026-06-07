# Pet4Net Updates

This repository hosts the public update manifest and release assets for the Pet4Net deployment system.

Pet4Net Manager uses this repository to check whether newer versions are available for:

* CONTROLLER firmware
* CAM firmware
* MikroTik captive portal files
* Pet4Net Manager desktop application

## Update Manifest

The main update manifest is:

```text
manifest.json
```

Pet4Net Manager reads this file to compare the installed version of each component with the latest available version.

Raw manifest URL:

```text
https://raw.githubusercontent.com/j102003/pet4net-updates/main/manifest.json
```

## Release Assets

Compiled update files are uploaded under GitHub Releases, not directly inside the repository.

Expected release assets:

```text
controller-vX.X.X.bin
cam-vX.X.X.bin
network-ui-vX.X.X.zip
Pet4Net-Manager-Setup-vX.X.X.exe
```

## Component Update Methods

| Component       | File Type | Update Method                                                        |
| --------------- | --------- | -------------------------------------------------------------------- |
| CONTROLLER      | `.bin`    | Pet4Net Manager downloads and uploads to the CONTROLLER OTA endpoint |
| CAM             | `.bin`    | Pet4Net Manager downloads and uploads to the CAM OTA endpoint        |
| MikroTik Portal | `.zip`    | Pet4Net Manager downloads and applies portal files to MikroTik       |
| Pet4Net Manager | `.exe`    | Pet4Net Manager downloads and launches the installer/update package  |

## Security Check

Each release file should include a SHA256 checksum in `manifest.json`.

Pet4Net Manager should verify the downloaded file before applying the update.

## Notice

This repository is only for deployment updates and release delivery.

It does not contain the full Pet4Net source code, training code, model source files, thesis source files, or private development materials.
