# IdcProbeV1
Invasive isolated DC Current probe based on Sensitec CMS3000

## What

This USB 5V powered current sensor should provide an relatively cheap way to safely scope AC or DC current.  
It should provide isolation up to 4 kV (rms), meaning it can measure anywhere in a circuit.

The high bandwidth and accuracy of the Sensitec module made it almost like a normal shunt.

Transfer ratio of the 5A and 15A unit would be 1A:1V and 1A:0.1V respectively.

## Challenges
The challenges involved in this project are powering the Sensitec sensor from a USB port, commonly found on most modern scopes.  
This required a high frequency (1.3 Mhz) DC-DC converter to create positive ands negative 12V for the sensor.  
Several prototypes have shown this is not an easy job, keeping ripple low is difficult with >1 MHz converters.

Due to the capacitance required for the DC-DC converter a high inrush current needs to be reduced on the USB input.

## Progress so far
So far has been two working prototypes (photo) have beed made and used thoroughly this year, it was extremely useful!  
Several important changes to the PCD have been made, both to the DC-DC, the input current, and output oscillation prevention on the output.

![photo of prototype](https://raw.githubusercontent.com/Jeroen6/IdcProbeV1/master/media/Prototype%20box.jpg)  
![photo of prototype](https://raw.githubusercontent.com/Jeroen6/IdcProbeV1/master/media/thumbnails/Prototype%201%20-%20top%20thumbnail.jpg)
![photo of prototype](https://raw.githubusercontent.com/Jeroen6/IdcProbeV1/master/media/thumbnails/Prototype%201%20-%20bottom%20left%20thumbnail.jpg)  
*(high-res in media folder)*

However, when time came to continue this project sad news arrived.  
[Sensitec discontinued the CMS and CDS current sensor families][1], with the [CFS1000][2] chip as alternative.

## Future
The CFS1000 is a more versatile product. Which is an advantage, but not if you required on the engineering and factory calibration of the CMS3000.
The CFS series requires development of an external sensing busbar and calibration procedure, both exceed my intended complexity of this project.

I will not persue development of this project, apart from assembling a few units for peronal use.  

*If someone has ideas to revive this project, let me know (make an issue or something)*

[1]: https://github.com/Jeroen6/IdcProbeV1/blob/master/doc/Sensitec%20-%20CMS3000%20-%20Current%20sensor%20discontinuation%20notice.pdf
[2]: https://github.com/Jeroen6/IdcProbeV1/blob/master/doc/Sensited%20-%20CFS1000%20-%20%20Integrated%20MagnetoResistive%20Current%20Sensor.pdf
