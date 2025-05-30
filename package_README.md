# Refloat

A full-featured self-balancing skateboard package.

## New in 1.1
- Haptic Feedback: Audible and vibrating feedback generated by the motor
- Parking Brake: A strong stand-still brake on 6.05 firmware
- Automatic backup and per-board backup in Settings -> Setup
- Improved setpoint smoothing for ATR and Torque Tilt
- Configurable order of LED strips and color order per strip
- Improved tune handling in AppUI
- Realtime Data Plotting and Recording: For developers and power users to analyze board behavior
- Many minor features and fixes

For more details, read the [1.1 release post](https://pev.dev/t/refloat-version-1-1/2480).

## Installation
### Upgrading
Back up your package config (either by **Backup Configs** on the Start page, or by saving the XML on **Refloat Cfg**), install the package and restore your config (**Restore Configs** or load the XML).

If you use Refloat for LED control, you'll need to re-configure a few options, these won't restore from your backup (make note of your current settings before upgrading):
- _Specs -> LED Mode_: set Internal if your _LED Type_ was **RGB** or **RGBW**
- _Specs -> Status / Front / Rear LED Color Order_
  - Pick an option with a **W** if your _LED Type_ was **RGBW**; Pick the RGB order that you had in your _LED Color Order_
  - Or, just keep trying them until the colors look correct (remember a restart is needed)
  - You need to set this for all of the three strips that you use

### Fresh Installation
If doing a fresh board installation, you need to do the **motor** and **IMU** calibration and configuration. If you install the package before that, you need to disable the package before running the **motor** _calibration_ and re-enable it afterwards.

For a detailed guide, read the [Initial Board Setup guide on pev.dev](https://pev.dev/t/initial-board-setup-in-vesc-tool/2190).

To configure the package, you only need to set the **Low and High Tiltback voltages** on the **Specs** tab of **Refloat Cfg**. These need to be set according to your battery specs.

The options in the other tabs are set to good starting values that should provide you with a well behaving, rideable board.

## Disclaimer
**Use at your own risk!** Electric vehicles are inherently dangerous, authors of this package shall not be liable for any damage or harm caused by errors in the software. Not endorsed by the VESC project.

## Credits
Author: Lukáš Hrázký

Original Float package authors: Mitch Lustig, Dado Mista, Nico Aleman

## Downloads and Changelogs
[https://github.com/lukash/refloat/releases](https://github.com/lukash/refloat/releases)
