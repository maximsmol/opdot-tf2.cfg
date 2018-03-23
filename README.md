# opdot-TF2
opdot-TF2 is a Team Fortress 2 configuration framework.

This README is a part of version 0.1.0.

## Table of Contents
1. [Overview](#overview)
1. [Installation](#installation)
    1. [Pre-packaged (recommended)](#pre-packaged-recommended)
    1. [From Source](#from-source)
1. [Usage](#usage)
1. [Design Goals](#design-goals)
1. [Design](#design)
1. [Credits](#credits)
1. [Et Cetera](#et-cetera)

## Overview
opdot-TF2 is an implementation of a new approach to TF2 configuration, but it is approximately equivalent to [mastercomfig](https://github.com/mastercoms/mastercomfig) version 6.2.1 if its more novel features are not used.

## Installation
### Pre-packaged (recommended)
No pre-packaged download is currently available. Do not expect one until a stable release (v1.0.0).

### From Source
Place the contents of the repository in the `steamapps/common/Team Fortress 2/tf/custom/opdot-tf2/cfg` folder (relative to your Steam installation). Create any folders that do not exist.

<!-- Depending on your operating system the full path typically is:

OS | Typical Path
---: | ---
Windows |
Linux | ``
Mac | `/Users/`username`/Library/Application Support/Steam/steamapps/common/Team Fortress 2/tf/custom/opdot-tf2/cfg` -->

## Usage
After installing the config it is recommended to amend some system-dependent defaults:
1. Start by creating a `main.cfg` under the `steamapps/common/Team Fortress 2/tf/cfg` folder (relative to your Steam installation).
1. Find the appropriate rate settings using mastercomfig's [rate calculator](https://mastercoms.github.io/mastercomfig/upload/). Put them in your `main.cfg`.
1. Add the module for your operating system
    1. For Linux add `exec os/linux`
    1. For Windows add `exec os/win`
    1. For Mac add `exec os/mac`
1. Choose the module appropriate for your hardware:

CPU Thread Count | SSD/HDD | Module
---: | :---: | ---
Only 1 | SSD | `exec hw/1_core/ssd`
Only 1 | HDD | `exec hw/1_core/hdd`
Less than 4 | SSD | `exec hw/no_4_cores/ssd`
Less than 4 | HDD | `exec hw/no_4_cores/hdd`
At least 4 | SSD | `exec hw/ssd`
At least 4 | HDD | `exec hw/hdd`

## Design Goals
Provide a comprehensive set of easily composable customization modules and the supporting infrastructure for:
- Optimization
- Visual customization via engine configuration
- Network settings
- Sane defaults
- Recommended gameplay settings
- Gameplay scripts
- Competitive play

🚫 The following are explicitly banned by design:
- Gameplay-altering modifications
- Modifications that replace any visuals, except those that only lower the quality of assets

The primary use for modules shall be the execution by the final user.

Modules shall be composable: they shall be compatible with as many 3rd-party customizations as possible. This shall be achieved through unambiguous, explicit and granular design.

Modules shall be expressive and safe: they shall make the wrong thing more difficult to do than the right thing. They shall not make anything impossible to do.

## Design
To be described

## Credits
❤ Presently, opdot-TF2 is a re-imagining of [mastercomfig](https://github.com/mastercoms/mastercomfig) version 6.2.1. Omitted content can be found in the respective `_omit.txt` files. Also see [`intentional_differences.txt`](intentional_differences.txt). Original license in [LICENSE_3RD_PARTY](LICENSE_3RD_PARTY).

## Et Cetera
Versions are bumped according to the [Semantic Versioning](https://semver.org/) specification.

Licensed under MIT (see [LICENSE](LICENSE) and [LICENSE_3RD_PARTY](LICENSE_3RD_PARTY)).
