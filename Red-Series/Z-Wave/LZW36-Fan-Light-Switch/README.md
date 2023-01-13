## <b>Inovelli Red Series Dimmer Switch</b>
*This is the repository for the Inovelli Red Series Switch that houses all firmware files along with release notes.*

### About

<img
     src = 'https://cdn.shopify.com/s/files/1/0612/9519/8373/products/InovelliFanLightSwitch_1800x1800.png.jpg?v=1659052277'
     alt = 'Inovelli Red Series 2-1  Fan Light Switch)'
     width = 400
/>

SKU: LZW31-SN

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

## V1.36 - 08/14/2020 
### Bug Fixes
- Fixed: Issue of Z-wave switch losing communication with fan module under certain scenarios. 
### Enhancements
- Add parameter 51, to enable instant on (ie: disable the 700ms delay). Note, if you disable the delay, it will also disable scene control except for Button 1 (ie: tap up 1x or tap down 1x, held & released) and button 6, 7, 8, 9 (level up / down buttons). All other scenes will be disabled.

<table>
<tr>
<th>Parameter</th>
<th>Size</th>
<th>Default</th>
<th>Range</th>
</tr>
<tr>
<td>51</td>
<td>1 Byte</td>
<td>0 - 1</td>
<td>
0: No Delay</br>
1: 700ms Delay</br></td>
</tr>
</table>
