# <b>Inovelli Red Series Dimmer Switch</b>
*This is the repository for the Inovelli Red Series Dimmer Switch that houses all firmware files along with release notes.*

### About

<img
     src = 'https://community.inovelli.com/uploads/default/original/2X/0/0f0a12c8d29b384ac98ee294585b69342662b4c9.png'
     alt = 'Inovelli Red Series Dimmer Switch'
     width = 400
/>

SKU: LZW31-SN

In each product's folder, you'll see all of the production firmware alongside a folder titled, "Beta". All of the production versions are considered stable and used for production, whereas the firmware in the "Beta" has not been fully tested and <b>should be used at your own risk</b>. We do our best to test it prior to releasing it, but there may be bugs that we didn't catch. Production firmware is what was put into production and is deemed stable.

### Disclaimer
The software is provided "as is" to provide our customers the ability to update our products.

Inovelli does not offer any express or implied warranty of any kind when using these files, including, but not limited to, warranties of merchantability, noninfringement, or fitness for a particular purpose. 

Inovelli does not imply or guarantee that the software provided will meet your requirements or that the operation thereof will be uninterrupted or error-free, or that all errors will be corrected.

Inovelli does not assume any responsibility for product errors related to the use of the software contained within this repository.

Inovelli does not offer support on flashing firmware to the devices listed here and are only provided as a courtesy to our customers and the community.

### BUGS / ENHANCEMENTS
If you find a bug and would like to report it, please open a **[Bug Report]** and we will take a look at our earliest convenience. If you would like an enhancement, please open an **[Firmware Request]** and we will also take a look at our earliest convenience. 

Please note that while enhancements may be requested, it may not always be possible for us to do -- we will try our best, but if it cannot be done, we will explain why.

***

## FIRMWARE CHANGELOG
Please see below for a summary of each version's changelog. Each version will also link to its respective parameter and Z-Wave documentation. For the most up-to-date parameter table, please visit the LZW31-SN **[Parameter Table]**. 

### V1.61 - 10/19/2021
- Fixed - Dimmer sending duplicate reports in certain scenarios while being controlled by certain hubs. 

***

### V1.57 - 06/29/2021
- Fixed - Optimization of Aux mode in neutral setting.
- Fixed - The inoperative issue after changing parameter 8 from high value to low value.

***

### V1.56 - 05/10/2021
- Fixed - Further optimization of Aux switch support in neutral and non-neutral. 

***

### V1.55 - 04/28/2021
- Fixed - When parameter 52 is set to 1 the physical button press would not turn the load off

***

### V1.54 - 04/26/2021
- Modify parameter 52 to provide 3 modes. 0 - Normal, 1 - On / Off only mode, 2 - Smart Bulb Mode
- Fixed - Aux Can Turn Off but Not On when in Non Neutral mode
- Fixed - Protection Set v1 Enabling Protection v2 Remote
- Fixed - Boot Loop Issue in Non-Neutral (Red, Green, Blue LED)
- Fixed - Aux Switch Not Causing Scenes to be Sent

***

### V1.53 - 03/10/2021

- 1.53 has been removed temporarily as it is missing some features that were not supposed to be removed. Version 1.54 will be released in its place.

***

### V1.52 - 01/22/2021
- Modified Smart Bulb Mode so that the output can only be turned off by sending a BasicSet(0x00).
- Fixed: Solve the problem that the power measured by the light is 5W when the load is not connected (caused by inaccurate power measurement at extremely low power consumption).

***

### V1.51 - 01/08/2021
- Fixed: Low brightness would brighten and then darken when being dimmed.
- Fixed: Issue where the same value of parameter 5 (Minimum Level) appears inconsistently when both parameters 21 (Power Type =1 - Neutral) and 22 (Switch Type = 1 – 3-Way) are set to 1.

***

### V1.49 - 12/16/2020
- Remove local configuration mode (to make space for extra features).
- Adding parameter 50 to adjust the delay when parameter 51 is set to 1. 1=100ms, 2=200ms, 3=300ms, etc.
- 2x taps on the config button will now send a configuration report of a value 0 to indicate the animation has stopped.
- Have device send “SwitchMultiLevelSet” every 1 second to associated devices as the device dims up & down for association group 3.
- Config Button 2x press will turn off a notification and also send a 2x pressed scene to the hub.

***

### V1.48 - 09/01/2020 
#### Bug Fixes
- Fixed: S2 bootstrapping issue. Improves S2 compatibility with 700 series hubs like Hubitat C-7.

***

### V1.47 - 07/17/2020 
#### Bug Fixes
- Fixed: Bug that when you select the parameter in local config mode and do not edit it. If you long press the config key to save it, it will set to 0.
- Fixed: If you are OTA during dimming, that will cause the bulb to flash.
- Fixed: when a device is not on a network, a factory reset by holding down the config button for 25 seconds does not reset the configuration. 
- Fixed: multiple switches blink green (like they were excluded)when more than one switch is not on a z-ware network and one of those switches is 

#### Enhancements
- Add parameter 51, to enable instant on (ie: disable the 700ms delay). Note, if you disable the delay, it will also disable scene control except for Button 1 (ie: tap up 1x or tap down 1x) and button 7 (config button). All other buttons (2-6) will be disabled.
- Parameter 51
Size: 1 Byte</br>
Default: 1</br>
Range: 0-1</br>
0: No Delay</br>
1: 700ms Delay</br>
- Added parameter 52. Use to put the switch into "smart bulb" mode. If it set to 1, the power will output maximum % when the dimmer is on. 0 = normal operation, 1 = smart bulb.

***

### V1.45 - 06/22/2020
### Enhancements
- Removed parameter 7 (Invert Switch) and parameter 10 (Default Level) in local configuration mode. This was to make room on the limited Z-wave 500 chip for the following changes:
- Increase the output ratio value on the PWM for better compatibility of Smart Bulbs when in single pole or aux switch mode.
- Added the ability to change the LED bar to white when parameter 13 is set to 255.

***

### V1.44 - 05/27/2020
#### Bug Fixes
- Fixed: Bug when double press the switch immediately after using up/down button causes the LED bar to be incorrect.
- Fixed: Holtek firmware was saving data too often causing the bulb to flicker. 

***

### V1.43 - 04/11/2020
#### Bug Fixes
- Fixed: Bug where parameter 5 could not be set below 10.
- Fixed: Bug that Switch Multilevel Start Level Change cannot change level below minimum level parameter number.
- Fixed: Bug that Switch Multilevel Start Level Change command can not set the association device brightness to 1%.
- Fixed: Bug where the LED bar would work abnormally when the local switch and aux switch are used together.
- Fixed: Bug that meter report is sent during dimming resulting in an inaccurate report.
- Fixed: Bug that power meter value is 0 when light brightness is 0.

### Enhancements
- Modify the default value of parameter 11 to 100.
- Change the calculation method of parameter 20. Change it from % to KWH. 0=0.01KWH, 10=0.1KWH, 100=1KWH; Modify the range value of parameter 20 to 0~127.
- Restart the "Safe guard" time of meter report when the level has been changed. The "Safe guard" timer is to prevent network flooding when device power fluctuates. 

***

### V1.41 - 03/28/2020
#### Bug Fixes
- Fixed Energy & power reporting not being disabled when configuration options are set to 0.
- Fixed Power reports flooding network when bulb power consumption fluctuates frequently. 
- Homeseer: Fixed not processing BasicReports when sent after turning switch on/off from the wall. Changed to SwitchMultiLevelReport.
- Vera: Fixed association purging issue. Vera was not properly processing group #4 group name. Shortened the name to resolve this issue.
- Fixed state sometimes not being restored properly when local protection is enabled.
- Fixed dimmer turning off when level rises above 80% on certain circuits. Make sure parameter 21 & 22 are set correctly.
- Fixed an issue where when the user sets parameter 5 in switch config mode it causes an exception.
- Fixed additional bugs for setting configuration parameters in switch config mode for parameters 5,9,10,11.
- Fixed an issue where holding the down key to adjust a device in association group 4 would sometimes turn it off.
- Fixed a bug where the duration of parameter 17 is far from the expected value.
- Fixed an issue where the interval time of Central Scene notification is far from the expected value.
- Fixed the issue of sending two Meter reports when the device is powered on.

#### Enhancements
- Notifications no longer turning off when user adjusts the level or performs various other actions on the switch.
- Changing minimum level to 10% to accommodate likely use of LED bulbs.
- Change the range of parameter 19 to 0,30-32767 to prevent users from choosing a value that may flood the network. 

<!----------------------------------------------------------------------------->

[Bug Report]: https://github.com/InovelliUSA/Firmware/issues/new?assignees=&labels=&template=firmware_bug_report.yml&title=%5BBug+Report%5D%3A+PRODUCT+-+FW+VERSION+-+HUB
[Firmware Request]: https://github.com/InovelliUSA/Firmware/issues/new?assignees=&labels=&template=firmware_request.yml&title=%5BFirmware+Request%5D%3A+PRODUCT+-+SUMMARY
[Parameter Table]: https://github.com/InovelliUSA/Firmware/blob/main/Red-Series/Z-Wave/LZW30-SN-On-Off-Switch/Parameter-Table.md
