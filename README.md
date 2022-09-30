<div align = center>

# [OpenledRace](https://github.com/ArminJo/OpenledRace)
An implementation of the OpenledRace Arduino game

[![Badge License: GPLv3](https://img.shields.io/badge/License-GPLv3-brightgreen.svg)](https://www.gnu.org/licenses/gpl-3.0)
 &nbsp; &nbsp; 
[![Badge Version](https://img.shields.io/github/v/release/ArminJo/OpenledRace?include_prereleases&color=yellow&logo=DocuSign&logoColor=white)](https://github.com/ArminJo/OpenledRace/releases/latest)
 &nbsp; &nbsp; 
[![Badge Commits since latest](https://img.shields.io/github/commits-since/ArminJo/OpenledRace/latest?color=yellow)](https://github.com/ArminJo/OpenledRace/commits/master)
 &nbsp; &nbsp; 
[![Badge Build Status](https://github.com/ArminJo/OpenledRace/workflows/TestCompile/badge.svg)](https://github.com/ArminJo/OpenledRace/actions)
 &nbsp; &nbsp; 
![Badge Hit Counter](https://visitor-badge.laobi.icu/badge?page_id=ArminJo_OpenledRace)
<br/>

**Extended version** of the OpenLedRace "version Basic for PCB Rome Edition. 2 Player, without Boxes Track".<br/>
Available as [OpenLedRace example](https://github.com/ArminJo/NeoPatterns/tree/master/examples/OpenLedRace) in the [NeoPatterns library](https://github.com/ArminJo/NeoPatterns).

</div>
<br/>

# Extensions to standard version
 *  **Input from MPU6050 Accelerometer**.
 *  Classes for Car, Bridge, Ramp and Loop with **natural gravity**.
 *  **Light effects** by NeoPattern library.
 *  **Tone generation without dropouts** by use of hardware timer output.
 *  2004 **LCD** for instructions and leap counter.
 *  Input feedback by an 8 pixel Neopixel bar.
 *  Winner melody by PlayRTTTL library.
 *  Compensation for blocked millis() timer during draw.
 *  Checks for RAM availability.
 *  Overlapping of cars is handled by using addPixelColor() for drawing.

 <br/>

# Principle of operation
With every button press or every acceleration of the dumbbells you **add a fixed amount of energy to the "car"**.<br/>
This energy is used to **increase speed**.

Formula is: **NewSpeed = sqrt((OldSpeed * OldSpeed) + AdditionalEnergy)**

On the other hand, **energy is consumed by friction and drag**.<br/>
Gravity also increases or decreases the car as in real life.

Formula is: **NewSpeed = OldSpeed + Gravity + Friction + (OldSpeed * Drag)**

<br/>

# Pictures
| At the Hannover MakerFaire 2022 | At the Cologne public library MINTköln-Festival 2021 |
| :-: | :-: |
| ![Accelerometer version from MakerFaire 2022](https://github.com/ArminJo/OpenledRace/blob/master/pictures/AcceleratorVersion.jpg) | ![OpenLedRace at the Cologne public library MINTköln-Festival](https://github.com/ArminJo/OpenledRace/blob/master/pictures/OpenLedRaceAtMintFestival.jpg) |

<br/>

# YouTube Videos
| At the Hannover MakerFaire 2022 | At the Cologne public library MINTköln-Festival 2021 |
| :-: | :-: |
| [![OpenLedRace at the Hannover MakerFaire 2022](https://i.ytimg.com/vi/lYzYpFYJfWI/hqdefault.jpg)](https://www.youtube.com/watch?v=lYzYpFYJfWI) | [![OpenLedRace in action](https://i.ytimg.com/vi/y25rjRkDg0g/hqdefault.jpg)](https://www.youtube.com/watch?v=y25rjRkDg0g) |


# Compile with the Arduino IDE
Download and extract the repository. In the Arduino IDE open the sketch with File -> Open... and select the OpenledRace folder.<br/>
You need to install *Adafruit NeoPixel* library under "Tools -> Manage Libraries..." or "Ctrl+Shift+I" -> use "neoPixel" as filter string.<br/>
You also need to install *NeoPatterns* and *PlayRtttl* library under "Tools -> Manage Libraries..." or "Ctrl+Shift+I"

### Based on:
- https://www.hackster.io/gbarbarov/open-led-race-a0331a
- https://twitter.com/openledrace
- https://gitlab.com/open-led-race
- https://openledrace.net/open-software/

#### If you find this program useful, please give it a star.
