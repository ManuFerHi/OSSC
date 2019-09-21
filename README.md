# OSSC [Open source scan converter]

![alt text](https://i.postimg.cc/pr5QGMW4/IMG-20181014-200007.jpg)

OSSC ManuFerHi version <BR>

<h2> <span class="mw-headline" id="Introduction"> Introduction </span></h2>
<p>The <b>O</b>pen <b>S</b>ource <b>S</b>can <b>C</b>onverter is a low-latency video digitizer and scan converter designed primarily for connecting retro video game consoles and home computers to modern displays. It converts analog RGB or component video signals into a digital format, and doubles (or triples) the scanlines of a single frame if necessary to generate a valid mode for digital TVs or monitors.
</p>
<h3> <span class="mw-headline" id="Features"> Features </span></h3>
<ul><li> Detection and digitization of various analog SDTV/EDTV/HDTV/PC modes
</li><li> Line double support for 240p, 480i, 288p, 576i, 384p, 480p, 576p
</li><li> Line3x/4x/5x support for 240p/288p with different sampling modes
</li><li> Very low latency (less than 2 input scanlines)
</li><li> Fast "deinterlace" for 480i/576i and 960i/1080i
</li><li> Fast recover from input video mode change (e.g. 240p&lt;-&gt;480i)
</li><li> All video processing done in RGB domain - no conversion to YCbCr
</li><li> Video and sync LPF for less-than optimal input signals
</li><li> Multiple inputs supporting various formats (see below)
</li><li> Full-range 24-bit RGB output through DVI/HDMI
</li><li> Emulated scanlines with configurable strength and position
</li><li> Configurable mask for overscan area
</li><li> Selectable sampling configuration for 480p input: DTV-480p or VGA 640x480
</li><li> Selectable CSC configuration for YPbPr source: Rec. 601 or Rec. 709
</li></ul>
</li></ul>
<h2> <span class="mw-headline" id="Power"> Power </span></h2>
<p>OSSC requires an external DC power supply. A unit that outputs 5 volts DC with at least 1 Amp will work. The tip must be 2.1 x 5.5mm and centre positive. 
</p><p>If desired, a USB to Barrel Jack adapter can be used. This will function correctly as long as the USB port or charger used in conjunction with OSSC outputs at least 1 amp of current. Such adapters can often be found on <a rel="nofollow" class="external text" href="https://www.amazon.co.uk/Barrel-Jack-Adapter-USB-5-5mm/dp/B00LX8MULA">Amazon</a> or other popular retailers.
</p><p>Do not use a power supply rated for AC output, or a power supply rated higher than 5 volts DC, doing so can damage the OSSC. 
</p><p>Using a supply that provides less than one amp of current may cause the OSSC to reset, especially when outputting at higher resolutions. You can however, safely use a PSU rated at least one amp or higher.
</p>
<h2> <span class="mw-headline" id="AV_inputs"> AV inputs </span></h2>
<h3> <span class="mw-headline" id="AV1_.28RGB-SCART.29"> AV1 (RGB-SCART) </span></h3>
<p>This input supports video in <b>RGBS</b>, <b>RGsB</b> (sync on green) and <b>YPbPr</b> formats. Composite video, luma or composite sync can be used as a sync source in RGBS mode. External sync splitters or boosters are generally not required or recommended as there is a built-in sync filter &amp; separator in the ADC frontend. The sync input has 75 ohm termination, so a TTL-level sync signal should not be directly connected to the OSSC in order to avoid unnecessarily stressing the source console and/or OSSC. A 470 ohm series resistor on the console side of the cable is generally a good solution when using cables which are wired for the TTL-level sync output of a console. The video inputs also have standard 75 ohm termination, so arcade boards may need extra resistors on the cable when connected directly without using a Supergun.
</p>
<h3> <span class="mw-headline" id="AV2_.28Component.29"> AV2 (Component) </span></h3>
<p>The AV2 input is a set of three RCA connectors which supports both component video (<b>YPbPr</b>) and RGB (<b>RGsB</b> format).
</p>
<h3> <span class="mw-headline" id="AV3_.28VGA.29"> AV3 (VGA) </span></h3>
<p>The AV3 input is a VGA/HD-15 connector which supports video in <b>RGBHV</b>, <b>RGBS</b> (pin 13), <b>RGsB</b> and <b>YPbPr</b> formats. RGBHV and RGBS modes require clean TTL-level sync signals and cannot extract sync from composite video or luma. AV3 is best suited for high-quality input sources as video LPF functionality is limited (the AV1 and AV2 inputs are routed through a dedicated LPF chip). Therefore, it is generally recommended to connect older consoles and arcade boards to these other inputs.
</p>
<h2> <span class="mw-headline" id="AV_outputs"> AV outputs </span></h2>
<h3> <span class="mw-headline" id="HDMI_.28DIY_boards.2C_v1.6_pre-assembled_boards.29"> HDMI (DIY boards, v1.6 pre-assembled boards) </span></h3>
<p>DIY and newer pre-assembled boards contain a HDMI connector which is used to transmit video data in 24bit RGB format. Digital audio output is available on v1.6 boards, while it can be added via an add-on board for earlier boards (see below) . Currents up to 200mA can be safely supplied via DDC 5V power pin to external devices such as active cables.
</p>
<h3> <span class="mw-headline" id="AV1_audio"> AV1 audio </span></h3>
<p>Analog audio from SCART input is bypassed to a 3.5mm stereo output jack next to video output connector. On v1.6 boards the jack alternatively functions as AV2 audio input, selectable via a miniature switch.


	

=======<BR>
For purchase OSSC visit my store http://www.manuferhi.com<BR>
For more information, contact with manuferhi@gmail.com






