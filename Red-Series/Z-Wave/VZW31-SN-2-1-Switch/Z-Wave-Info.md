## OVERVIEW
Please use this document as a resource to understand the various association groups, command classes, and meter info on your switch. We try to keep this up-to-date, but as we constantly change our firmware, there may be a mistake. Please reach out if you see anything that needs to be corrected.

We recommend you look at the firmware version your switch is on and then go directly into the corresponding folder and read the release notes for the most up-to-date information on your specific firmware version.

## ASSOCIATION GROUPS

<div class="tg-wrap"><table>
<thead>
  <tr>
    <th>Grouping Identifier</th>
    <th>Max Nodes</th>
    <th>Send Commands</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td rowspan="5">Group 1</td>
    <td rowspan="5">10</td>
    <td>1. Central Scene Notification</td>
  </tr>
  <tr>
    <td>2. Multilevel Report</td>
  </tr>
  <tr>
    <td>3. Protection Report</td>
  </tr>
  <tr>
    <td>4. Device Reset Locally</td>
  </tr>
  <tr>
    <td>5. Meter Report</td>
  </tr>
  <tr>
    <td>Group 2</td>
    <td>10</td>
    <td>Basic Set</td>
  </tr>
  <tr>
    <td>Group 3</td>
    <td>10</td>
    <td>Switch Multilevel Set</td>
  </tr>
  <tr>
    <td>Group 4</td>
    <td>10</td>
    <td>Switch Multilevel Start/Stop</td>
  </tr>
  <tr>
    <td>Group 5</td>
    <td>10</td>
    <td>Double-Tap Basic Set</td>
  </tr>
  <tr>
    <td>Group 6</td>
    <td>10</td>
    <td>Triple-Tap Basic Set</td>
  </tr>
</tbody>
</table></div>

**Group 1: Lifeline**
<br>
Members of this group will receive unsolicited messages related to the status of the switch

**Group 2: Basic Set**
<br>
Sends On & Off commands to associated devices
1. Single press on the up button sends BasicSet (0xFF)
2. Single press on the down button sends BasicSet (0x00)

**Group 3: Switch Multilevel Set**
<br>
Sends set level commands to associated devices when switch is pressed.
1. Release up or down button sends Switch MultiLevelSet which keeps
associated devices in sync with this device
2. Single press on the up button sends SwitchMultiLevelSet (0xFF)
3. Single press on the down button sends SwitchMultiLevelSet (0x00)
4. If param. 53 = 1, 2x press up sends SwitchMultiLevelSet to P55
5. If param. 54 = 1, 2x press down sends SwitchMultiLevelSet to P56

**Group 4: Switch Multilevel Start/Stop**
<br>
Sends start / stop level change to associated devices (only in dimmer mode)
1. Hold up button sends SW_MULTILEVEL_START_LEVEL_CHANGE (Up)
2. Hold down button sends SW_MULTILEVEL_START_LEVEL_CHANGE (Down)
3. Release either button sends SW_MULTILEVEL_STOP_LEVEL_CHANGE

**Group 5 & 6: Double or Triple-Tap Basic Set**
<br>
Sends On & Off commands to associated devices
1. 2x/3x press on the up button sends BasicSet (0xFF)
2. 2x/3x press on the down button sends BasicSet (0x00)

## SECURITY 2 COMMAND CLASSES
<div class="tg-wrap"><table>
<thead>
  <tr>
    <th>Command Class</th>
    <th>Version</th>
    <th>Required Security Class</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td> Z-Wave Plus Info </td>
    <td> V2 </td>
    <td> None </td>
  </tr>
  <tr>
    <td> Switch Multilevel </td>
    <td> V4 </td>
    <td> S0/S2 </td>
  </tr>
  <tr>
    <td> Configuration </td>
    <td> V4 </td>
    <td> S0/S2 </td>
  </tr>
  <tr>
    <td> Central Scene </td>
    <td> V3 </td>
    <td> S0/S2 </td>
  </tr>
  <tr>
    <td> Association </td>
    <td> V3 </td>
    <td> S0/S2 </td>
  </tr>
  <tr>
    <td> Multi-Channel Association </td>
    <td> V3 </td>
    <td> S0/S2 </td>
  </tr>
  <tr>
    <td> Association Group Information </td>
    <td> V3 </td>
    <td> S0/S2 </td>
  </tr>
  <tr>
    <td> Transport Service </td>
    <td> V2 </td>
    <td> None </td>
  </tr>
  <tr>
    <td> Version </td>
    <td> V3 </td>
    <td> S0/S2 </td>
  </tr>
  <tr>
    <td> Manufacturer Specific </td>
    <td> V2 </td>
    <td> S0/S2 </td>
  </tr>
  <tr>
    <td> Device Reset Locally </td>
    <td> V1 </td>
    <td> S0/S2 </td>
  </tr>
  <tr>
    <td> Indicator </td>
    <td> V3 </td>
    <td> S0/S2 </td>
  </tr>
  <tr>
    <td> Powerlevel </td>
    <td> V1 </td>
    <td> S0/S2 </td>
  </tr>
  <tr>
    <td> Security 0 </td>
    <td> V1 </td>
    <td> None </td>
  </tr>
  <tr>
    <td> Security 2 </td>
    <td> V1 </td>
    <td> None </td>
  </tr>
  <tr>
    <td> Supervision </td>
    <td> V1 </td>
    <td> None </td>
  </tr>
  <tr>
    <td> Firmware Update Meta Data </td>
    <td> V5 </td>
    <td> S0/S2 </td>
  </tr>
  <tr>
    <td> Meter </td>
    <td> V3 </td>
    <td> S0/S2 </td>
  </tr>
  <tr>
    <td> Protection </td>
    <td> V2 </td>
    <td> S0/S2 </td>
  </tr>
</tbody>
</table></div>

## METER INFO
Meter Type: 0x01 - Electric Meter
<br>
Meter Scale: 0x00 - kwh
<br>
Meter Scale: 0x02 - W
<br>
Rate Type: 0x01 - Import only (consumed)

## MULTILEVEL SWITCH DEVICE TYPE BASIC MAPPING
- Basic Set (Value) maps to Multilevel Switch Set (Value)
- Basic Report (Current Value, Duration) maps to Multilevel Switch
Report (Value, Duration)
