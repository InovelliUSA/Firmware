## OVERVIEW
Please use this document as a resource to understand the various parameters on your switch. We try to keep this up-to-date, but as we constantly change our firmware, there may be a mistake. Please reach out if you see anything that needs to be corrected.

We recommend you look at the firmware version your switch is on and then go directly into the corresponding folder and read the release notes for the most up-to-date information on your specific firmware version.

## PARAMETERS
Below we will describe the various parameters as well as list the most recent firmware parameter numbers, bytes, etc. Again, please double check these against the RELEASE NOTES in each firmware file folder.

### Firmwave Version 0.03
Date in Production: March 2023

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
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Dimming Speed (↑) - Remote<br/><br/><b/>Dimmer Mode Only</td>
<td>How fast or slow the light turns on when you change the dim level remotely (ie: dimming from 10-20%, 60-80%, etc)<br><details><summary><b>More Details</b></summary><br>0 = Instant On<br>5 = Fast (500ms)<br>126 = Slow (12.6s)<br><br><b>IF USING A DUMB SWITCH:</b> This parameter will not work when pressing the dumb switch manually.<br><b>NOTE:</b> Third party code may need to be implemented (device handler, driver, etc) for this to work properly. Some hubs may not support this feature.</details></td>
<td>0-126</td>
<td>25 <br>(2.5s)</td>
<td>1</td>
</tr>
<tr>
<td>2</td>
<td>Dimming Speed (↑) - Local<br><br><b>Dimmer Mode Only</b></td>
<td>How fast or slow the light the light turns on when you hold up on the switch (ie: dimming from 10-20%, 60-80%, etc)<details><summary><b>More Details</b></summary><br>0 = Instant On<br>5 = Fast (500ms)<br>126 = Slow (12.6s)<br>127 = Sync to Parameter 1<br><br><b>IF USING A DUMB SWITCH:</b> This parameter will not work when pressing the dumb switch manually.</details></td>
<td>0-127</td>
<td>127</td>
<td>1</td>
</tr>
<tr>
<td>3</td>
<td>Ramp Rate (Off → On) - Remote<br><br><b>Dimmer Mode Only</b></td>
<td>How fast or slow the light turns on when you remotely bring the switch from Off to On<details><summary><b>More Details</b></summary><br>0 = Instant On<br>5 = Fast (500ms)<br>126 = Slow (12.6s)<br>127 = Sync to Parameter 1<br><br><b>NOTE:</b> Third party code may need to be implemented (device handler, driver, etc) for this to work properly. Some hubs may not support this feature.</td>
<td>0-127</td>
<td>127</td>
<td>1</td>
</tr>
<tr>
<td>4</td>
<td>Ramp Rate (Off → On) - Local<br><br><b>Dimmer Mode Only</b></td>
<td>How fast or slow the light turns on when you press the switch up 1x to bring from Off to On<details><summary><b>More Details</b></summary><br>0 = Instant On<br>5 = Fast (500ms)<br>126 = Slow (12.6s)<br>127 = Sync to Parameter 3</td>
<td>0-127</td>
<td>127</td>
<td>1</td>
</tr>
<tr>
<td>5</td>
<td>Dimming Speed (↓) - Remote<br><br><b>Dimmer Mode Only</b></td>
<td>How fast or slow the light turns off when you change the dim level remotely (ie: dimming from 80-60%, 20-10%, etc)<details><summary><b>More Details</b></summary><br>0 = Instant Off<br>5 = Fast (500ms)<br>126 = Slow (12.6s)<br>127 = Sync to Parameter 1<br><br><b>IF USING A DUMB SWITCH:</b> This parameter will not work when pressing the dumb switch manually.<br><b>NOTE:</b> Third party code may need to be implemented (device handler, driver, etc) for this to work properly. Some hubs may not support this feature.</td>
<td>0-127</td>
<td>127</td>
<td>1</td>
</tr>
<tr>
<td>6</td>
<td>Dimming Speed (↓) - Local<br><br><b>Dimmer Mode Only</b></td>
<td>How fast or slow the light the light turns off when you hold down on the switch (ie: dimming from 80-60%, 20-10%, etc)<details><summary><b>More Details</b></summary><br>0 = Instant Off<br>5 = Fast (500ms)<br>126 = Slow (12.6s)<br>127 = Sync to Parameter 2<br><br><b>IF USING A DUMB SWITCH:</b> This parameter will not work when pressing the dumb switch manually.</td>
<td>0-127</td>
<td>127</td>
<td>1</td>
</tr>
<tr>
<td>7</td>
<td>Ramp Rate (On → Off) - Remote<br><br><b>Dimmer Mode Only</b></td>
<td>How fast or slow the light turns on when you remotely bring the switch from Off to On<details><summary><b>More Details</b></summary><br>0 = Instant Off<br>5 = Fast (500ms)<br>126 = Slow (12.6s)<br>127 = Sync to Parameter 3<br><b>NOTE:</b> Third party code may need to be implemented (device handler, driver, etc) for this to work properly. Some hubs may not support this feature.</td>
<td>0-127</td>
<td>127</td>
<td>1</td>
</tr>
<tr>
<td>8</td>
<td>Ramp Rate (On → Off) - Local<br><br><b>Dimmer Mode Only</b></td>
<td>How fast or slow the light turns on when you press the switch up 1x to bring from Off to On<details><summary><b>More Details</b></summary><br>0 = Instant Off<br>5 = Fast (500ms)<br>126 = Slow (12.6s)<br>127 = Sync to Parameter 4</td>
<td>0-127</td>
<td>127</td>
<td>1</td>
</tr>
<tr>
<td>9</td>
<td>Minimum Dim Level<br><br><b>Dimmer Mode Only</b></td>
<td>Minimum level the light switch will dim to<details><summary><b>More Details</b></summary><br>Lower the numeric value = lower the min dim level (1 = ~1%)<br><br>Higher the numeric value = higher the min dim level (254 = ~99%)<br><br>Great for fixing flickering bulbs or calibrating the bulb if it shuts off prior to 1%<br><br><b>HUB NOTE:</b> Some hub user interfaces may show a range of 1-99 as available inputs. This is because it&#39;s easier to think in terms of 0-100% instead of calculating what number out of 255 is equal to x%.</td>
<td>1-254</td>
<td>1</td>
<td>1</td>
</tr>
<tr>
<td>10</td>
<td>Maximum Dim Level<br><br><b>Dimmer Mode Only</b></td>
<td>Maximum level the light switch will dim to<details><summary><b>More Details</b></summary><br>Lower the numeric value = lower the max dim level (2 = ~2%)<br><br>Higher the numeric value = higher the max dim level (255 = ~100%)<br><br><b>NOTE:</b> Great for calibrating a bulb when it reaches maximum level before 100%<br><br><b>HUB NOTE:</b> Some hub user interfaces may show a range of 2-100 as available inputs. This is because it&#39;s easier to think in terms of 0-100% instead of calculating what number out of 255 is equal to x%.</td>
<td>2-255</td>
<td>255</td>
<td>1</td>
</tr>
<tr>
<td>11</td>
<td>Invert Switch</td>
<td>Inverts the switch  (Tapping ↓ = On, Tapping ↑ = Off)<details><summary><b>More Details</b></summary><br>0 = Disabled<br>1 = Enabled</td>
<td>0-1</td>
<td>0</td>
<td>1</td>
</tr>
<tr>
<td>12</td>
<td>Auto Off Timer</td>
<td>Automatically turns the switch off after x amount of seconds<details><summary><b>More Details</b></summary><br>0 = Disabled<br>1 = 1s<br>32767 = 32767s</td>
<td>0-32767</td>
<td>0</td>
<td>2</td>
</tr>
<tr>
<td>13</td>
<td>Default Level - Local<br><br><b>Dimmer Mode Only</b></td>
<td>The default dim level the switch goes to when turned on locally (at the switch)<details><summary><b>More Details</b></summary><br>0 = Off<br>1-254 = Specific level on<br>255 = Returns to prior state it was before being turned off<br><br><b>HUB NOTE:</b> Some hub user interfaces may show a range of 1-100 as available inputs. This is because it&#39;s easier to think in terms of 0-100% instead of calculating what number out of 255 is equal to x%.</td>
<td>0-255</td>
<td>255</td>
<td>1</td>
</tr>
<tr>
<td>14</td>
<td>Default Level - Remote<br><br><b>Dimmer Mode Only</b></td>
<td>The default dim level the switch goes to when powered on via a remote command<details><summary><b>More Details</b></summary><br>0 = Off<br>1-254 = Specific level on<br>255 = Returns to prior state it was before being turned off<br><br><b>HUB NOTE:</b> Some hub user interfaces may show a range of 1-100 as available inputs. This is because it&#39;s easier to think in terms of 0-100% instead of calculating what number out of 255 is equal to x%.</td>
<td>0-255</td>
<td>255</td>
<td>1</td>
</tr>
<tr>
<td>15</td>
<td>Level After Power Restored</td>
<td>When power is restored, the switch reverts to either On, Off, or Last Level<details><summary><b>More Details</b></summary><br>0 = Off<br>1-254 = Specific level on<br>255 = Returns to level before power outage</td>
<td>0-255</td>
<td>255</td>
<td>1</td>
</tr>
<tr>
<td>17</td>
<td>LED Indicator Timeout</td>
<td>Changes the amount of time (in seconds) the RGB Bar shows the Dim level<details><summary><b>More Details</b></summary><br>0 = Always off<br>1 = 1 second after level is adjusted<br>10 = 10 seconds after level is adjusted<br>11 = Always on</td>
<td>0-11</td>
<td>11</td>
<td>1</td>
</tr>
<tr>
<td>18</td>
<td>Active Power Reports</td>
<td>The power level change that will result in a new power report being sent in wattage (W)<details><summary><b>More Details</b></summary><br>0 = Disabled<br>1 = 0.1W change<br>10 = 1W change<br>100 = 10W change<br>32767 = 3276.7W</td>
<td>0-32767</td>
<td>10</td>
<td>2</td>
</tr>
<tr>
<td>19</td>
<td>Periodic Power &amp; Energy Reports</td>
<td>Time period between consecutive power and energy reports being sent (in seconds)<details><summary><b>More Details</b></summary><br>0 = Disabled<br>1 = 1s<br>32767 = 32767s<br><br>NOTE: Timer resets after every report is sent</td>
<td>0-32767</td>
<td>3600</td>
<td>2</td>
</tr>
<tr>
<td>20</td>
<td>Energy Reports</td>
<td>The energy level change that will result in a new energy report being sent in kilowatt hours (kWh)<details><summary><b>More Details</b></summary><br>0 = Disabled<br>1 = 0.01kWh<br>10 = 0.1kWh<br>100 = 1kWh<br>32767 = 327.67kWh</td>
<td>0-32767</td>
<td>10</td>
<td>2</td>
</tr>
<tr>
<td>21</td>
<td>AC Power Type</td>
<td>Select whether you are wiring your switch with or without a neutral wire<details><summary><b>More Details</b></summary><br>0 = No-Neutral<br>1 = Neutral</td>
<td>0-1</td>
<td>1</td>
<td>1</td>
</tr>
<tr>
<td>22</td>
<td>Switch Type</td>
<td>Select what type of installation you have<details><summary><b>More Details</b></summary><br>0 = Single-Pole (ie: one switch)<br>1 = Multi-Way (Dumb Switch)<br>2 = Multi-Way (Auxiliary Switch)</td>
<td>0-2</td>
<td>0</td>
<td>1</td>
</tr>
<tr>
<td>50</td>
<td>Switch Delay</td>
<td>Adjusts the delay between taps in 100ms increments<br>0 = 0ms (disables multi-tap scene control), 1 = 100ms, 2 = 200ms, 9 = 900ms)</td>
<td>0-9</td>
<td>7</td>
<td>1</td>
</tr>
<tr>
<td>52</td>
<td>Smart Bulb Mode</td>
<td>Enables or disables smart bulb mode<details><summary><b>More Details</b></summary><br>0 = Disable SBM<br>1 = Enable SBM</td>
<td>0-1</td>
<td>0</td>
<td>1</td>
</tr>
<tr>
<td>95</td>
<td>LED Indicator Color (When On) - LED #&#39;s 1-7</td>
<td>This will set the default color of the LED Bar (all 7 LED&#39;s) when the switch is on<details><summary><b>More Details</b></summary><br>Calculated by using a hue color circle (Value / 255 * 360). See website for more info.</td>
<td>0-255</td>
<td>170 (Blue)</td>
<td>3</td>
</tr>
<tr>
<td>96</td>
<td>LED Indicator Color (When Off) - LED #&#39;s 1-7</td>
<td>This will set the default color of the LED Bar (all 7 LED&#39;s) when the switch is off<details><summary><b>More Details</b></summary><br>Calculated by using a hue color circle (Value / 255 * 360). See website for more info.</td>
<td>0-255</td>
<td>170 (Blue)</td>
<td>3</td>
</tr>
<tr>
<td>97</td>
<td>LED Indicator Intensity (When On) - LED #&#39;s 1-7</td>
<td>This will set the intensity (ie: how bright it is) of the LED bar (all 7 LED&#39;s) when the switch is on<details><summary><b>More Details</b></summary><br>0 = Off<br>10 = Low<br>50 = Medium<br>100 = High</td>
<td>0-100</td>
<td>33</td>
<td>1</td>
</tr>
<tr>
<td>98</td>
<td>LED Indicator Intensity (When Off) - LED #&#39;s 1-7</td>
<td>This will set the intensity (ie: how bright it is) of the LED bar (all 7 LED&#39;s) when the switch is off<details><summary><b>More Details</b></summary><br>0 = Off<br>10 = Low<br>50 = Medium<br>100 = High</td>
<td>0-100</td>
<td>1</td>
<td>1</td>
</tr>
<tr>
<td>256</td>
<td>Local Protection</td>
<td>Determines whether or not the load of the switch can be controlled via paddle presses (locally)<details><summary><b>More Details</b></summary><br>0 = Disabled<br>1 = Enabled</td>
<td>0-1</td>
<td>0</td>
<td>1</td>
</tr>
<tr>
<td>257</td>
<td>Remote Protection</td>
<td>Determines whether or not the load of the switch can be controlled via RF (remote)<details><summary><b>More Details</b></summary><br>0 = Disabled<br>1 = Enabled</td>
<td>0-1</td>
<td>0</td>
<td>1</td>
</tr>
<tr>
<td>258</td>
<td>Switch Mode (Dimmer or On/Off)</td>
<td>Determines the mode of the switch (On/Off or Dimmer)<details><summary><b>More Details</b></summary><br>0 = On/Off<br>1 = Dimmer</td>
<td>0-1</td>
<td>0</td>
<td>1</td>
</tr>
<tr>
<td>259</td>
<td>One LED Mode</td>
<td>Switch only shows LED #1 and does not show LED #&#39;s 2-6 -- this mimics the Red Series On/Off switch<details><summary><b>More Details</b></summary><br>0 = Disabled<br>1 = Enabled</td>
<td>0-1</td>
<td>0</td>
<td>1</td>
</tr>
<tr>
<td>260</td>
<td>Firmware Progress LED</td>
<td>During a firmware update, the switch will show the progress on the LED Bar<details><summary><b>More Details</b></summary><br>EXAMPLE: 1/4 LED Bar shown = 25%, 1/2 LED Bar shown = 50%, 3/4 LED Bar shown = 75%<br><br>0 = Disable, 1 = Enable</td>
<td>0-1</td>
<td>1</td>
<td>1</td>
</tr>
<tr>
<td>261</td>
<td>Disable Relay, &quot;Click&quot; Sound</td>
<td>In neutral on/off setups, the default is to have a clicking sound to notify you that the relay is open or closed. You may disable this sound by creating a, &quot;simulated&quot; on/off where the switch only will turn onto 100 or off to 0.<details><summary><b>More Details</b></summary><br>0 = Disabled (Click Sound On)<br>1 = Enabled (Click Sound Off</td>
<td>0-1</td>
<td>0</td>
<td>1</td>
</tr>
</tbody>
</table>
