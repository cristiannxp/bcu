# bcu (Board Control Utilities)

[![Build status](https://github.com/nxp-imx/bcu/actions/workflows/main.yml/badge.svg?branch=master)](https://github.com/nxp-imx/bcu/actions/workflows/main.yml/badge.svg?branch=master)
![GitHub](https://img.shields.io/github/license/nxp-imx/bcu.svg)
[![Coverity Scan Build Status](https://scan.coverity.com/projects/18825/badge.svg)](https://scan.coverity.com/projects/nxpmicro-bcu)

[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-white.svg)](https://snapcraft.io/bcu-nxp)
  - Install
    - $ sudo snap install --devmode bcu-nxp; sudo snap alias bcu-nxp bcu
  - Upgrade
    - $ sudo snap refresh bcu-nxp --devmode

_______________________________________________________________________________________________________
## **For more details about BCU, please check the BCU release note(BCU.pdf) in the latest release page.**
_______________________________________________________________________________________________________

# **Running environment**

 - Windows 10/11, 64bit
    - Need install FTDI Driver for Windows.
    - Early Windows version(below 1.2.0) need install vs2017 redistribute package

 - Ubuntu 16.04 or above, or **all Linux distribution**, 64bit
    - Get it from the Snap Store:
      - $ sudo snap install --devmode bcu-nxp; sudo snap alias bcu-nxp bcu
    - If you do not want to run BCU as root in Linux, please follow the steps below to set the rules.
      - $ cd /etc/udev/rules.d/
      - $ sudo vim xx-ftdi.rules
      - Add the line to this file: 
      ```
      SUBSYSTEMS=="usb", ATTRS{idVendor}=="0403", ATTRS{idProduct}=="6011", GROUP="dialout", MODE="0660"
      ```
      - Save the file
      - Re-plug the debug wire
    - To upgrade to the latest BCU version, please use this command: 
      - $ sudo snap refresh bcu-nxp --devmode

 - Ubuntu 18.04 or above, 64bit, using binary provided from release page
    - Need install these libraries
      - $ sudo apt-get install libftdi1-2 libyaml-dev libconfuse-dev
    - If you do not want to run BCU as root in Linux, please follow the steps below to set the rules.
      - $ cd /etc/udev/rules.d/
      - $ sudo vim xx-ftdi.rules
      - Add the line to this file: 
      ```
      SUBSYSTEMS=="usb", ATTRS{idVendor}=="0403", ATTRS{idProduct}=="6011", GROUP="dialout", MODE="0660"
      ```
      - Save the file
      - Re-plug the debug wire

 - Mac OS 11.x Big Sur or above, x64
    - Need install Homebrew first
      - $ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    - Then install other libs by Homebrew
      - $ brew install libftdi libyaml
 - Mac OS 11.x Big Sur or above, arm64
    - Apple Silicon can run x64 binary, but all libs should be installed to the path which is same as x64.
      - $ arch -x86_64 $SHELL
      - $ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    - Install other libs by Homebrew to default path(/usr/local/Cellar)
      - $ brew install libftdi libyaml

# **Board support**

## i.MX8MP-EVK

- imx8mpevk
- imx8mpevkpwra0
- imx8mpevkpwra1
- imx8mpddr3l
- imx8mpddr4

## i.MX8DXL-EVK

- imx8dxlevk
- imx8dxl_ddr3_evk
- imx8dxl_obx

## i.MX8ULP-EVK

- imx8ulpevk
- imx8ulpevk9
- imx8ulpwatchval
- imx8ulpwatchuwb

## i.MX93

- imx93evk11/imx93evk11b1
- imx93qsb
- imx93evk14

## i.MX91

- imx91evk11
- imx91qsb

## i.MX95

- imx95evk19
- imx95evk15

## i.MX943

- imx943evk19a0/imx943evk19b1


_______________________________________________________________________________________________________

## To get support:

 - From NXP internal issue: Create Jira ticket in MLK project, component TOOLS
 - From Customers: Create new Issue in this repo https://github.com/nxp-imx/bcu


_______________________________________________________________________________________________________

