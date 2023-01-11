## OVERVIEW
Please use this document as a resource to understand the various parameters on your switch. We try to keep this up-to-date, but as we constantly change our firmware, there may be a mistake. Please submit a [CORRECTION REPORT] if you see anything that needs to be corrected.

We recommend you look at the firmware version your switch is on and then go directly into the corresponding folder and read the release notes for the most up-to-date information on your specific firmware version.

## PARAMETERS
Below we will describe the various parameters as well as list the most recent firmware parameter numbers, bytes, etc. Again, please double check these against the RELEASE NOTES in each firmware file folder.

### Firmwave Version 0.03
Date in Production: March 2023

<table>
  <tr>
    <th>#</th>
    <th>Parameter Name</th>
    <th>Byte Size</th>
    <th>Range</th>
    <th>Description</th>
    <th>Default</th>
  </tr>
  <tr>
    <td>1</td>
    <td>Dimming Speed (Dimming Up)</td>
    <td>1</td>
    <td>0-254</td>
    <td>This changes the speed in which the attached light dims up or down when controlled from the physical switch
      <br><br>
      Test test test tes
  </tr>
  <tr>
    <td>Centro comercial Moctezuma</td>
    <td>Francisco Chang</td>
    <td>Mexico</td>
  </tr>
</table>



<table>
  <tr>
    <th>Parameter</th>
    <th>Range</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><strong>Parameter 1</strong <br> Dimming Speed (Dimming Up)</td>
    <td>[1 Byte], 0-254</td>
    <td>This changes the speed in which the attached light dims up or down when controlled from the physical switch</td>
  </tr>
  <tr>
    <td>Centro comercial Moctezuma</td>
    <td>Francisco Chang</td>
    <td>Mexico</td>
  </tr>
</table>



<b>Parameter # 1:</b>	Dimming Speed (Dimming Up)
<br>
<b>Byte Size:</b> 1	
<br>
Range: 0-254	
<br>
Description: This changes the speed in which the attached light dims up or down. A setting of 0 should turn the light immediately on or off (almost like an on/off switch). Increasing the value should slow down the transition speed.
<ul>
  <li>0-100 in ms, (0-10000 ms)</li>
  <li>101-160 in seconds, (1-59 seconds)</li>
  <li>161 - 254 in minutes (1-93 minutes)"</li>
</ul>

2	Dimming Speed (From Switch) (Dimming Up)	1	0-255	"Now in 100ms. This changes the speed in which the attached light dims up or down when controlled from the physical switch. A setting of 0 should turn the light immediately on or off (almost like an on/off switch). Increasing the value should slow down the transition speed. A setting of 255 should keep this in sync with parameter 1.

0-100 in ms, (0-10000 ms) (not support 1~4)
101-160 in seconds, (1-59 seconds)
161 - 254 in minutes (1-93 minutes)
255- Keep in sync with parameter 1
