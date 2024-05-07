# Zephyr™ Mechanical Keyboard (ZMK) Firmware

[![Discord](https://img.shields.io/discord/719497620560543766)](https://zmk.dev/community/discord/invite)
[![Build](https://github.com/zmkfirmware/zmk/workflows/Build/badge.svg)](https://github.com/zmkfirmware/zmk/actions)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-v2.0%20adopted-ff69b4.svg)](CODE_OF_CONDUCT.md)

[ZMK Firmware](https://zmk.dev/) is an open source ([MIT](LICENSE)) keyboard firmware built on the [Zephyr™ Project](https://www.zephyrproject.org/) Real Time Operating System (RTOS). ZMK's goal is to provide a modern, wireless, and powerful firmware free of licensing issues.

Check out the website to learn more: https://zmk.dev/.

You can also come join our [ZMK Discord Server](https://zmk.dev/community/discord/invite).

To review features, check out the [feature overview](https://zmk.dev/docs/). ZMK is under active development, and new features are listed with the [enhancement label](https://github.com/zmkfirmware/zmk/issues?q=is%3Aissue+is%3Aopen+label%3Aenhancement) in GitHub. Please feel free to add 👍 to the issue description of any requests to upvote the feature.

Toolchain Installation

Install West

```
pip3 install -U west
```

Clone the repository

```
git clone git@github.com:hw-tinkerers/zmk.git
```

Navigate to the folder

```
cd zmk
```

Initialize the Application

```
west init -l app/
```

Update to Fetch Modules

```
west update
```

Export Zephyr CMake package
This allows CMake to load the code needed to build ZMK

```
west zephyr-export
```

Install Zephyr Python Dependencies

```
pip3 install -r zephyr/scripts/requirements.txt
```

Build for TR60 using

```
west build -p always -b tr60 app/
```

Flash the UF2 firmware found in DIR build/zephyr/zmk.uf2
