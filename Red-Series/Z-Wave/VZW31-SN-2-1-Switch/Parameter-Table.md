## OVERVIEW
Please use this document as a resource to understand the various parameters on your switch. We try to keep this up-to-date, but as we constantly change our firmware, there may be a mistake. Please reach out if you see anything that needs to be corrected.

We recommend you look at the firmware version your switch is on and then go directly into the corresponding folder and read the release notes for the most up-to-date information on your specific firmware version.

## PARAMETERS
Below we will describe the various parameters as well as list the most recent firmware parameter numbers, bytes, etc. Again, please double check these against the RELEASE NOTES in each firmware file folder.

### Firmwave Version 1.00
Date in Production: April 2023
<br>Date Code: 2304

**NOTE:** Some parameters are only available in dimmer mode and are called out in the, "About" section with the words, "Dimmer Mode Only".

<table>
<thead>
<tr>
<th>#</th>
<th>About</th>
<th>Description</th>
<th>Range</th>
<th>Default</th>
<th>Size (Bytes)</th>
<th>Firmware Version Implemented</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Dimming Speed (↑) - Remote<br/><br/><b/>Dimmer Mode Only</td>
<td>How fast or slow the light turns on when you change the dim level remotely (ie: dimming from 10-20%, 60-80%, etc)<br><details><summary><b>More Details</b></summary><br>0 = Instant On<br>5 = Fast (500ms)<br>126 = Slow (12.6s)<br><br><b>IF USING A DUMB SWITCH:</b> This parameter will not work when pressing the dumb switch manually.<br><b>NOTE:</b> Third party code may need to be implemented (device handler, driver, etc) for this to work properly. Some hubs may not support this feature.</details></td>
<td>0-254</td>
<td>25 <br>(2.5s)</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>2</td>
<td>Dimming Speed (↑) - Local<br><br><b>Dimmer Mode Only</b></td>
<td>How fast or slow the light the light turns on when you hold up on the switch (ie: dimming from 10-20%, 60-80%, etc)<details><summary><b>More Details</b></summary><br>0 = Instant On<br>5 = Fast (500ms)<br>126 = Slow (12.6s)<br>255 = Sync to Parameter 1<br><br><b>IF USING A DUMB SWITCH:</b> This parameter will not work when pressing the dumb switch manually.</details></td>
<td>0-255</td>
<td>255</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>3</td>
<td>Ramp Rate (Off → On) - Remote<br><br><b>Dimmer Mode Only</b></td>
<td>How fast or slow the light turns on when you remotely bring the switch from Off to On<details><summary><b>More Details</b></summary><br>0 = Instant On<br>5 = Fast (500ms)<br>126 = Slow (12.6s)<br>255 = Sync to Parameter 1<br><br><b>NOTE:</b> Third party code may need to be implemented (device handler, driver, etc) for this to work properly. Some hubs may not support this feature.</td>
<td>0-255</td>
<td>255</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>4</td>
<td>Ramp Rate (Off → On) - Local<br><br><b>Dimmer Mode Only</b></td>
<td>How fast or slow the light turns on when you press the switch up 1x to bring from Off to On<details><summary><b>More Details</b></summary><br>0 = Instant On<br>5 = Fast (500ms)<br>126 = Slow (12.6s)<br>255 = Sync to Parameter 3</td>
<td>0-255</td>
<td>255</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>5</td>
<td>Dimming Speed (↓) - Remote<br><br><b>Dimmer Mode Only</b></td>
<td>How fast or slow the light turns off when you change the dim level remotely (ie: dimming from 80-60%, 20-10%, etc)<details><summary><b>More Details</b></summary><br>0 = Instant Off<br>5 = Fast (500ms)<br>126 = Slow (12.6s)<br>127 = Sync to Parameter 1<br><br><b>IF USING A DUMB SWITCH:</b> This parameter will not work when pressing the dumb switch manually.<br><b>NOTE:</b> Third party code may need to be implemented (device handler, driver, etc) for this to work properly. Some hubs may not support this feature.</td>
<td>0-255</td>
<td>255</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>6</td>
<td>Dimming Speed (↓) - Local<br><br><b>Dimmer Mode Only</b></td>
<td>How fast or slow the light the light turns off when you hold down on the switch (ie: dimming from 80-60%, 20-10%, etc)<details><summary><b>More Details</b></summary><br>0 = Instant Off<br>5 = Fast (500ms)<br>126 = Slow (12.6s)<br>127 = Sync to Parameter 2<br><br><b>IF USING A DUMB SWITCH:</b> This parameter will not work when pressing the dumb switch manually.</td>
<td>0-255</td>
<td>255</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>7</td>
<td>Ramp Rate (On → Off) - Remote<br><br><b>Dimmer Mode Only</b></td>
<td>How fast or slow the light turns on when you remotely bring the switch from Off to On<details><summary><b>More Details</b></summary><br>0 = Instant Off<br>5 = Fast (500ms)<br>126 = Slow (12.6s)<br>255 = Sync to Parameter 3<br><b>NOTE:</b> Third party code may need to be implemented (device handler, driver, etc) for this to work properly. Some hubs may not support this feature.</td>
<td>0-255</td>
<td>255</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>8</td>
<td>Ramp Rate (On → Off) - Local<br><br><b>Dimmer Mode Only</b></td>
<td>How fast or slow the light turns on when you press the switch up 1x to bring from Off to On<details><summary><b>More Details</b></summary><br>0 = Instant Off<br>5 = Fast (500ms)<br>126 = Slow (12.6s)<br>255 = Sync to Parameter 4</td>
<td>0-255</td>
<td>255</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>9</td>
<td>Minimum Dim Level<br><br><b>Dimmer Mode Only</b></td>
<td>Minimum level the light switch will dim to<details><summary><b>More Details</b></summary><br>Lower the numeric value = lower the min dim level (1 = ~1%)<br><br>Higher the numeric value = higher the min dim level (54 = 99%)<br><br>Great for fixing flickering bulbs or calibrating the bulb if it shuts off prior to 1%</td>
<td>1-54</td>
<td>1</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>10</td>
<td>Maximum Dim Level<br><br><b>Dimmer Mode Only</b></td>
<td>Maximum level the light switch will dim to<details><summary><b>More Details</b></summary><br>Lower the numeric value = lower the max dim level (2 = ~2%)<br><br>Higher the numeric value = higher the max dim level (99 = 99%)<br><br><b>NOTE:</b> Great for calibrating a bulb when it reaches maximum level before 99%</td>
<td>55-99</td>
<td>99</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>11</td>
<td>Invert Switch</td>
<td>Inverts the switch  (Tapping ↓ = On, Tapping ↑ = Off)<details><summary><b>More Details</b></summary><br>0 = Disabled<br>1 = Enabled</td>
<td>0-1</td>
<td>0</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>12</td>
<td>Auto Off Timer</td>
<td>Automatically turns the switch off after x amount of seconds<details><summary><b>More Details</b></summary><br>0 = Disabled<br>1 = 1s<br>32767 = 32767s</td>
<td>0-32767</td>
<td>0</td>
<td>2</td>
<td>1.00+</td>
</tr>
<tr>
<td>13</td>
<td>Default Level - Local<br><br><b>Dimmer Mode Only</b></td>
<td>The default dim level the switch goes to when turned on locally (at the switch)<details><summary><b>More Details</b></summary><br>1-99 = Specific level on<br>0 = Returns to prior state it was before being turned off</td>
<td>0-99</td>
<td>0</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>14</td>
<td>Default Level - Remote<br><br><b>Dimmer Mode Only</b></td>
<td>The default dim level the switch goes to when powered on via a remote command<details><summary><b>More Details</b></summary><br>1-99 = Specific level on<br>0 = Returns to prior state it was before being turned off</td>
<td>0-99</td>
<td>0</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>15</td>
<td>Level After Power Restored</td>
<td>When power is restored, the switch reverts to either On, Off, or Last Level<details><summary><b>More Details</b></summary><br>0 = Off<br>1-99 = Specific level on<br>100 = Returns to level before power outage</td>
<td>0-100</td>
<td>100</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>17</td>
<td>LED Indicator Timeout</td>
<td>Changes the amount of time (in seconds) the RGB Bar shows the Dim level<details><summary><b>More Details</b></summary><br>0 = Always off<br>1 = 1 second after level is adjusted<br>10 = 10 seconds after level is adjusted<br>11 = Always on</td>
<td>0-11</td>
<td>11</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>18</td>
<td>Active Power Reports</td>
<td>The power level change that will result in a new power report being sent in wattage (W)<details><summary><b>More Details</b></summary><br>0 = Disabled<br>1 = 0.1W change<br>10 = 1W change<br>100 = 10W change<br>32767 = 3276.7W</td>
<td>0-32767</td>
<td>10</td>
<td>2</td>
<td>1.00+</td>
</tr>
<tr>
<td>19</td>
<td>Periodic Power &amp; Energy Reports</td>
<td>Time period between consecutive power and energy reports being sent (in seconds)<details><summary><b>More Details</b></summary><br>0 = Disabled<br>1 = 1s<br>32767 = 32767s<br><br>NOTE: Timer resets after every report is sent</td>
<td>0-32767</td>
<td>3600</td>
<td>2</td>
<td>1.00+</td>
</tr>
<tr>
<td>20</td>
<td>Energy Reports</td>
<td>The energy level change that will result in a new energy report being sent in kilowatt hours (kWh)<details><summary><b>More Details</b></summary><br>0 = Disabled<br>1 = 0.01kWh<br>10 = 0.1kWh<br>100 = 1kWh<br>32767 = 327.67kWh</td>
<td>0-32767</td>
<td>10</td>
<td>2</td>
<td>1.00+</td>
</tr>
<tr>
<td>21</td>
<td>AC Power Type</td>
<td>Select whether you are wiring your switch with or without a neutral wire<details><summary><b>More Details</b></summary><br>0 = No-Neutral<br>1 = Neutral</td>
<td>0-1</td>
<td>1</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>22</td>
<td>Aux Switch Type & Full Sine Mode</td>
<td>Select the Aux Switch type as well as Full Sine Mode<details><summary><b>More Details</b></summary><br>0 = None<br>1 = 3-Way Dumb Switch<br>2 = 3-Way Aux Switch<br>3 = Single Pole Full Sine Wave</td>
<td>0-3</td>
<td>0</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>25</td>
<td>Higher Output in Non-Neutral</td>
<td>Ability to increase level in non-neutral mode but may cause problems with high level ficker or aux switch detection. Adjust max level (P10) if you have problems with this enabled.<details><summary><b>More Details</b></summary><br>0 = Disabled <br>1 = Enabled</td>
<td>0-1</td>
<td>0</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>50</td>
<td>Button Press Delay</td>
<td>Adjusts the delay between button taps in 100ms increments<br>0 = 0ms / No Delay (disables multi-tap scene control), 1 = 100ms, 2 = 200ms, 9 = 900ms)</td>
<td>0-9</td>
<td>5</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>52</td>
<td>Smart Bulb Mode</td>
<td>Enables or disables smart bulb mode<details><summary><b>More Details</b></summary><br>0 = Disable SBM<br>1 = Enable SBM</td>
<td>0-1</td>
<td>0</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>53</td>
<td>Double-Tap Up to Parameter 55<br/><br/><b/>Dimmer Mode Only</td>
<td>Enable or Disable setting brightness to parameter 55 on double-tap up.<details><summary><b>More Details</b></summary><br>0 = Disabled<br>1 = Enabled</td>
<td>0-1</td>
<td>0</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>54</td>
<td>Double-Tap Down to Parameter 56<br/><br/><b/>Dimmer Mode Only</td>
<td>Enable or Disable setting brightness to parameter 56 on double-tap down.<details><summary><b>More Details</b></summary><br>0 = Disabled<br>1 = Enabled</td>
<td>0-1</td>
<td>0</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>55</td>
<td>Brightness Level for Double-Tap Up<br/><br/><b/>Dimmer Mode Only</td>
<td>Set this level on double-tap up (if enabled by P53)<details><summary><b>More Details</b></summary><br>1 = 1%<br>2 = 2%<br>99 = 99%</td>
<td>1-99</td>
<td>99</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>56</td>
<td>Brightness Level for Double-Tap Down<br/><br/><b/>Dimmer Mode Only</td>
<td>Set this level on double-tap down (if enabled by P54)<details><summary><b>More Details</b></summary><br>0 = off<br>1 = 1%<br>2 = 2%<br>99 = 99%</td>
<td>0-99</td>
<td>1</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>58</td>
<td>Exclusion Behavior</td>
<td>How the device behaves during exclusion<details><summary><b>More Details</b></summary><br>0 = LED Bar Does Not Pulse (when config tapped 3x)<br>1 = LED Bar pulses blue<br>2 = Device does not enter exclusion mode (requires factory reset to leave network or change this parameter)</td>
<td>0-2</td>
<td>1</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>59</td>
<td>Association Behavior</td>
<td>Choose when the switch sends commands to associated devices<details><summary><b>More Details</b></summary><br>0 = Never<br>1 = Local<br>2 = Z-Wave<br>3 = Both</td>
<td>0-3</td>
<td>1</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>64</td>
<td>LED #1 Notification</td>
<td>A 4-Byte encoded LED Notification for LED #1 (bottom LED)<details><summary><b>More Details</b></summary><br>To see an example, please go to the following URL: https://inovelliusa.github.io/inovelli-switch-toolbox/ and select, "VZW31-SN" under the "Switch Type" dropdown. Then select, "1" under where it says, "LED" and then play with the values (Color, Brightness, Duration, etc).</td>
<td>0-4294967295</td>
<td>0</td>
<td>4</td>
<td>1.00+</td>
</tr>
<td>69</td>
<td>LED #2 Notification</td>
<td>A 4-Byte encoded LED Notification for LED #2 (second from the bottom LED)<details><summary><b>More Details</b></summary><br>To see an example, please go to the following URL: https://inovelliusa.github.io/inovelli-switch-toolbox/ and select, "VZW31-SN" under the "Switch Type" dropdown. Then select, "2" under where it says, "LED" and then play with the values (Color, Brightness, Duration, etc).</td>
<td>0-4294967295</td>
<td>0</td>
<td>4</td>
<td>1.00+</td>
</tr>
<td>74</td>
<td>LED #3 Notification</td>
<td>A 4-Byte encoded LED Notification for LED #3 (third from the bottom LED)<details><summary><b>More Details</b></summary><br>To see an example, please go to the following URL: https://inovelliusa.github.io/inovelli-switch-toolbox/ and select, "VZW31-SN" under the "Switch Type" dropdown. Then select, "3" under where it says, "LED" and then play with the values (Color, Brightness, Duration, etc).</td>
<td>0-4294967295</td>
<td>0</td>
<td>4</td>
<td>1.00+</td>
</tr>
<td>79</td>
<td>LED #4 Notification</td>
<td>A 4-Byte encoded LED Notification for LED #4 (middle LED)<details><summary><b>More Details</b></summary><br>To see an example, please go to the following URL: https://inovelliusa.github.io/inovelli-switch-toolbox/ and select, "VZW31-SN" under the "Switch Type" dropdown. Then select, "4" under where it says, "LED" and then play with the values (Color, Brightness, Duration, etc).</td>
<td>0-4294967295</td>
<td>0</td>
<td>4</td>
<td>1.00+</td>
</tr>
<td>84</td>
<td>LED #5 Notification</td>
<td>A 4-Byte encoded LED Notification for LED #5 (third from the top LED)<details><summary><b>More Details</b></summary><br>To see an example, please go to the following URL: https://inovelliusa.github.io/inovelli-switch-toolbox/ and select, "VZW31-SN" under the "Switch Type" dropdown. Then select, "5" under where it says, "LED" and then play with the values (Color, Brightness, Duration, etc).</td>
<td>0-4294967295</td>
<td>0</td>
<td>4</td>
<td>1.00+</td>
</tr>
<td>89</td>
<td>LED #6 Notification</td>
<td>A 4-Byte encoded LED Notification for LED #6 (second from the top LED)<details><summary><b>More Details</b></summary><br>To see an example, please go to the following URL: https://inovelliusa.github.io/inovelli-switch-toolbox/ and select, "VZW31-SN" under the "Switch Type" dropdown. Then select, "6" under where it says, "LED" and then play with the values (Color, Brightness, Duration, etc).</td>
<td>0-4294967295</td>
<td>0</td>
<td>4</td>
<td>1.00+</td>
</tr>
<td>94</td>
<td>LED #7 Notification</td>
<td>A 4-Byte encoded LED Notification for LED #7 (top LED)<details><summary><b>More Details</b></summary><br>To see an example, please go to the following URL: https://inovelliusa.github.io/inovelli-switch-toolbox/ and select, "VZW31-SN" under the "Switch Type" dropdown. Then select, "7" under where it says, "LED" and then play with the values (Color, Brightness, Duration, etc).</td>
<td>0-4294967295</td>
<td>0</td>
<td>4</td>
<td>1.00+</td>
</tr>
<tr>
<td>95</td>
<td>LED Indicator Color (When On) - LED #&#39;s 1-7</td>
<td>This will set the default color of the LED Bar (all 7 LED&#39;s) when the switch is on<details><summary><b>More Details</b></summary><br>0 = Red<br>14 = Orange<br>35 = Lemon<br>64 = Lime<br>85 = Green<br>106 = Teal<br>127 = Cyan<br>149 = Aqua<br>170 = Blue<br>191 = Violet<br>212 = Magenta<br>234 = Pink<br>255 = White</td>
<td>0-255</td>
<td>170 (Blue)</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>96</td>
<td>LED Indicator Color (When Off) - LED #&#39;s 1-7</td>
<td>This will set the default color of the LED Bar (all 7 LED&#39;s) when the switch is off<details><summary><b>More Details</b></summary><br>0 = Red<br>14 = Orange<br>35 = Lemon<br>64 = Lime<br>85 = Green<br>106 = Teal<br>127 = Cyan<br>149 = Aqua<br>170 = Blue<br>191 = Violet<br>212 = Magenta<br>234 = Pink<br>255 = White</td>
<td>0-255</td>
<td>170 (Blue)</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>97</td>
<td>LED Indicator Intensity (When On) - LED #&#39;s 1-7</td>
<td>This will set the intensity (ie: how bright it is) of the LED bar (all 7 LED&#39;s) when the switch is on<details><summary><b>More Details</b></summary><br>0 = Off<br>10 = Low<br>50 = Medium<br>100 = High</td>
<td>0-100</td>
<td>33</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>98</td>
<td>LED Indicator Intensity (When Off) - LED #&#39;s 1-7</td>
<td>This will set the intensity (ie: how bright it is) of the LED bar (all 7 LED&#39;s) when the switch is off<details><summary><b>More Details</b></summary><br>0 = Off<br>10 = Low<br>50 = Medium<br>100 = High</td>
<td>0-100</td>
<td>1</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>99</td>
<td>All LED Notification</td>
<td>A 4-Byte encoded LED Notification for LED's 1-7 (all LED's)<details><summary><b>More Details</b></summary><br>To see an example, please go to the following URL: https://inovelliusa.github.io/inovelli-switch-toolbox/ and select, "VZW31-SN" under the "Switch Type" dropdown. Then select, "All" under where it says, "LED" and then play with the values (Color, Brightness, Duration, etc).</td>
<td>0-4294967295</td>
<td>0</td>
<td>4</td>
<td>1.00+</td>
</tr>
<tr>
<td>100</td>
<td>LED Bar Scaling<br/><br/><b/>Dimmer Mode Only</td>
<td>Method used for LED Bar scaling.  This allows you to match the scaling when two different generations are in the same gang box (ie: Gen 2 LZW31, LZW31-SN vs Gen 3 VZW31-SN)<details><summary><b>More Details</b></summary><br>0 = Gen 3 (VZW)<br>1 = Gen 2 (LZW)</td>
<td>0-1</td>
<td>0</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>123</td>
<td>Aux Switch Unique Scenes</td>
<td>Have unique scene numbers for scenes activated with the aux switch. In other words, you can activate Scene A (multi-tap) from the smart switch and activate Scene B (multi-tap) from the auxiliary switch with the same number of multi-taps.<details><summary><b>More Details</b></summary><br>0 = Disabled<br>1 = Enabled</td>
<td>0-1</td>
<td>0</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>158</td>
<td>Switch Type</td>
<td>Select what type of installation you have<details><summary><b>More Details</b></summary><br>0 = Single-Pole (ie: one switch)<br>1 = Multi-Way (Dumb Switch)<br>2 = Multi-Way (Auxiliary Switch)</td>
<td>0-2</td>
<td>0</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>159</td>
<td>LED Bar in On/Off Switch Mode<br/><br/><b/>On/Off Mode Only</td>
<td>When the device in in On/Off Mode, use the Full LED Bar or just one LED<details><summary><b>More Details</b></summary><br>0 = Full Bar<br>1 = One LED</td>
<td>0-1</td>
<td>0</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>160</td>
<td>Firmware Update-in-Progress Bar</td>
<td>Display the firmware update progress on the LED Bar<details><summary><b>More Details</b></summary><br>0 = Disabled<br>1 = Enabled</td>
<td>0-1</td>
<td>1</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>161</td>
<td>Relay Click</td>
<td>Audible click in On/Off Mode<details><summary><b>More Details</b></summary><br>0 = Enabled<br>1 = Disabled</td>
<td>0-1</td>
<td>1</td>
<td>1</td>
<td>1.00+</td>
</tr>
<tr>
<td>162</td>
<td>Double-Tap Config/Favorites Button to Clear Notification</td>
<td>Double-Tap the config/favorites button to clear notifications<details><summary><b>More Details</b></summary><br>0 = Enabled<br>1 = Disabled</td>
<td>0-1</td>
<td>0</td>
<td>1</td>
<td>1.00+</td>
</tr>
</tbody>
</table>
