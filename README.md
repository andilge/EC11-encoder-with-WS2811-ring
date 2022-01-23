![The PCB](https://github.com/andilge/EC11-encoder-with-WS2811-ring/blob/main/images/board-front-and-back.png?raw=true)

# Rotary encoder with a 10 WS2811 F5 LEDs segmented ring on a translucent blank cover panel
A DIY controller interface for lights with coloured LEDs.

## Credits
The idea is inspired by my [Futai RGB encoder, 12 WS2811 F5 LED ring on a translucent blank cover panel](https://github.com/andilge/Futai-Encoder-WS2811-ring "my Futai RGB encoder, 12 WS2811 F5 LED ring on a translucent blank cover panel"). It basically grades down to one board with one encoder without RBD LED per translucent blank cover panel.

It was composed as add on for my [8 channel LED constant current driver board](https://github.com/andilge/8ch-constant-current-LED-driver "8 channel LED constant current driver board").

## Parts list
The folder 'fabrication' contains the zipped production files for pcb ordering and interactive bill of material ibom.html with purchase links for the components.

Additional to this you can purchase 10 blind plates also on [aliexpress.com](https://www.aliexpress.com/item/32884601740.html "aliexpress.com").

### Connector pinout
| silkscreen | description                                      |
|:----------:|--------------------------------------------------|
| G          | Ground                                           |
| SW         | Switch. Pressing it pulls down the pin to ground |
| B          | Encoder B                                        |
| A          | Encoder A                                        |
| SW         | Data in                                          |
| 5V         | 5 Volt                                           |


### SPECIAL ATTENTION REQUIRED !
*There are reports about wrong pin out for the addressable LEDs (D1-D10)*

The [official data sheet from the producer](http://cn.world-semi.com/DownLoadFile/98 "official data sheet from the producer") says
|  pin # |   description   |
|:------:|:---------------:|
|   1    |       DOUT      |
|   2    |       VCC       |
|   3    |       GND       |
|   4    |       DIN       |


With the purchase URL in the BOM, you might get LEDs with 180 degree flipped around pin out
|  pin # |   description   |
|:------:|:---------------:|
|   1    |       DIN       |
|   2    |       GND       |
|   3    |       VCC       |
|   4    |       DOUT      |

If you solder these faulty LEDs on the board "the right way around", no light turns on and the LEDs instantly burn off to nirvana, some with, others without magic smoke :astonished: rip

The board continues following the LED's specification and can handle these faulty LEDs if you just place them "the wrong way around". Basically, flipped pins together with flipped placement turns out as success again :man_facepalming:.

**IMPORTANT**: Please test a LED from the sent bunch first to get a reality approach about which way around you should use them !

## Tools list
### Required
- A soldering iron
- Solder

### Optional
- For SMD components and adressable LEDs:
  - A hot air soldering/re-flow station. However, the smallest parts are 0805 SMD components which can be soldered with a soldering iron. The LED's legs are very close together and easier to solder with hot air.
  - Solder paste
- Tweezers
- the famous IKEA cork coaster (Onderzetter) that gently takes up the heat of your soldering tools

