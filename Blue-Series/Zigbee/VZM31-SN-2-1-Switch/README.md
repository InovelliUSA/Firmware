# <b>Inovelli Blue Series On/Off Dimmer Switch</b>
*This is the repository for the Inovelli Blue Series Switch that houses all firmware files along with release notes.*

### About

<img
     src = 'https://cdn.shopify.com/s/files/1/0612/9519/8373/products/Inovelli2-1SwitchBlueSeriesSinglePack-VZM31-SN_1800x1800.png.jpg?v=1661975270'
     alt = 'Inovelli Blue Series 2-1 Switch On/Off'
     width = 400
/>

SKU: VZM31-SN

Each folder will have the words, "Beta" or "Production" next to the firmware file indicating what type of firmware is in each folder. **Beta firmware may be unstable and should be used at your own risk.** We do our best to test it prior to releasing it, but there may be bugs that we didn't catch. Production firmware is what was put into production and is deemed stable.

### Disclaimer
The software is provided "as is" to provide our customers the ability to update our products.

Inovelli does not offer any express or implied warranty of any kind when using these files, including, but not limited to, warranties of merchantability, noninfringement, or fitness for a particular purpose. 

Inovelli does not imply or guarantee that the software provided will meet your requirements or that the operation thereof will be uninterrupted or error-free, or that all errors will be corrected.

Inovelli does not assume any responsibility for product errors related to the use of the software contained within this repository.

Inovelli does not offer support on flashing firmware to the devices listed here and are only provided as a courtesy to our customers and the community.

### Bugs / Enhancements
If you find a bug and would like to report it, please open a **[Bug Report]** and we will take a look at our earliest convenience. If you would like an enhancement, please open an **[Enhancement Request]** and we will also take a look at our earliest convenience. 

Please note that while enhancements may be requested, it may not always be possible for us to do -- we will try our best, but if it cannot be done, we will explain why.

# Changelog

### November 11, 2022 / v2.08 / 0x01020208

**Note: We are waiting for a PR to go through for HA before releasing it there. Should be released on Hubitat soon. Bump ZHA quirks lib to 0.0.86 by dmulcahey · Pull Request #81966 · home-assistant/core (github.com) 60**

- Fix the ability to send commands to a group binding.
### November 8, 2022 / v2.07 / 0x01020207

**Note: It looks like 2.07 introduces a bug with group binding control and it is currently required that you use individual device binding. I’ll post an update when this gets resolved.**

- Remove the sending of multicast commands to avoid switches that would accidentally control other devices within a group.
- Fix the wrong destination endpoint used when sending some commands.
### November 7, 2022 / v2.06 / 0x01020206

- Fix for devices that are bound to the switch not using speed parameters 1-8.
### November 4, 2022 / v2.05 / 0x01020205

- Add parameter 262: Disable the “double tap” to clear notifications feature. Users can make it so family members do not clear notifications at the switch. (2.02)
- Improve the speed of sending power reports when load changes from on-to-off or off-to-on. (2.02)
- Added LED notifications: “falling”, “rising”, “aurora single”, and others. (2.02)
- Fix the bug that changes Philips Hue color temperature when dimming down. (2.03)
- Fix for device binding to Innr and possibly other devices. (2.05)
- Ability to change max level in On/Off 3-way dumb mode to accommodate special scenarios. (2.05)
