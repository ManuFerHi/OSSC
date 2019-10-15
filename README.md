# OSSC [Open source scan converter]

![alt text](https://i.postimg.cc/g0xtpX0W/IMG-20191015-211618.jpg)

OSSC ManuFerHi version <BR>

![alt text](https://i.postimg.cc/jq6bm99h/IMG-20191015-184713-1.jpg)

![alt text](https://i.postimg.cc/LXdc0B37/Ossc-remote2.jpg)

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
<h3> <span class="mw-headline" id="HDMI_.28DIY_boards.2C_v1.6_pre-assembled_boards.29"> HDMI </span></h3>
<p>HDMI connector which is used to transmit video data in 24bit RGB format. Currents up to 200mA can be safely supplied via DDC 5V power pin to external devices such as active cables.
</p>
<h3> <span class="mw-headline" id="AV1_audio"> AV1 audio </span></h3>
<p>Analog audio from SCART input is bypassed to a 3.5mm stereo output jack next to video output connector. The jack alternatively functions as AV2 audio input, selectable via a miniature switch.
</p>
<h2> <span class="mw-headline" id="Basic_usage"> Basic usage </span></h2>
<h3> <span class="mw-headline" id="Remote_control"> Remote control </span></h3>
<div class="thumb tright"><div class="thumbinner" style="width:394px;"><a href="Ossc_remote2.jpg" class="image"><img alt="" src="/xrgb/images/9/9b/Ossc_remote2.jpg" width="392" height="500" class="thumbimage" /></a>  <div class="thumbcaption">Default remote control keymap</div></div></div>
<p>The OSSC is available with a pre-programmed infrared remote. This is optional, and can be replaced with a suitable programmable/learning remote if desired).
</p>
<ul><li> 0-9: Selects AV source and input format. See remote picture on the side for reference.
</li><li> MENU: Activates/deactivates menu at on-board character LCD display
</li><li> OK: Selects sub-menu or function
</li><li> BACK: Returns to previous menu level or from info page to normal source display page
</li><li> UP/DOWN: Selects next/previous menu option
</li><li> LEFT/RIGHT: Option value -/+
</li><li> INFO: Displays extra information on video source processing. Top row shows current profile and current video mode preset. Bottom row shows accurate timing data from FPGA: lines per frame, p/i status, special processing (indicated by *) and cycles per frame (divide 27000000 by it to get Hz),
</li><li> LCD_BACKLIGHT: Turns on-board character LCD backlight off/on
</li><li> SCANLINE_MODE: Hotkey for selecting next "Scanlines" option value
</li><li> SCANLINE_TYPE: Hotkey for selecting next "Scanline type" option value
</li><li> SCANLINE_INT+/-: Hotkeys for adjusting scanline strength
</li><li> LINEMULT_MODE: Hotkey for selecting line multiplication mode for current video mode
</li><li> SAMP_PHASE+/-: Hotkey for sampling phase adjustment
</li><li> PROFILE_LOAD: Hotkey for quickloading a profile. Press again to enable selection of profiles 10 and higher
</li></ul>
<h3> <span class="mw-headline" id="PCB_buttons"> PCB buttons </span></h3>
<ul><li> BTN0: Next input/mode
</li><li> BTN1: Select between scanlines off/auto/manual
</li></ul>
<h3> <span class="mw-headline" id="Status_LEDs"> Status LEDs </span></h3>
<ul><li> Green: Power on. Light off when IR remote code detected
</li><li> Red: Unstable sync when alight.
</li></ul>
<h2> <span class="mw-headline" id="Settings"> Settings </span></h2>
<h3> <span class="mw-headline" id="Video_in_proc"> Video in proc </span></h3>
<h4> <span class="mw-headline" id="Video_LPF"> Video LPF </span></h4>
<p><i>Video low-pass filter. Filters out high-frequency noise on video, and can reduce jitter when sampling clock does not match input video dot clock rate (e.g. older consoles in linedouble mode). NOTE: The last 3 settings are not effective with VGA input in RGBHV/RGBS mode.</i>
</p>
<ul><li> <b>Auto</b>: Suitable LPF is automatically selected based on input source and video mode <b>[default]</b>
</li><li> <b>Off</b>: LPF is disabled.
</li><li> <b>95MHz (HDTV II)</b>: 95MHz bandwidth – suitable for 1080p
</li><li> <b>35MHz (HDTV I)</b>: 35MHz bandwidth – suitable for 720p
</li><li> <b>16MHz (EDTV)</b>: 16MHz bandwidth – suitable for 480p etc. EDTV formats
</li><li> <b>9MHz (SDTV)</b>: 9MHz bandwidth – suitable for 240p, 480i etc. SDTV formats
</li></ul>
<h4> <span class="mw-headline" id="YPbPr_input_Color_Space"> YPbPr input Color Space </span></h4>
<p><i>Controls YPbPr-&gt;RGB colorspace conversion coefficients.</i>
</p>
<ul><li> <b>Rec. 601</b>: Input is assumed to be in Rec. 601 format, which is generally true for SD video <b>[default]</b>
</li><li> <b>Rec. 709</b>: Input is assumed to be in Rec. 709 format, which is generally true for HD video
</li><li> <b>Auto</b>: Rec. 601 is used for SD input, Rec. 709 for HD (720p and higher)
</li></ul>
<h4> <span class="mw-headline" id="R.2FPr_.2F_G.2FY_.2F_B.2FPb_offset"> R/Pr / G/Y / B/Pb offset </span></h4>
<p>Fine-adjustment of Red/Pr / G/Y / B/Pb channel offset (brightness)
</p>
<ul><li> <b>0-255</b>: <b>[default=127]</b>
</li></ul>
<h4> <span class="mw-headline" id="R.2FPr_.2F_G.2FY_.2F_B.2FPb_gain"> R/Pr / G/Y / B/Pb gain </span></h4>
<p>Fine-adjustment of Red/Pr / G/Y / B/Pb channel gain (contrast)
</p>
<ul><li> <b>0-255</b>: <b>[default=26]</b>
</li></ul>
<h4> <span class="mw-headline" id="Pre-ADC_Gain"> Pre-ADC Gain </span></h4>
<p>Coarse-adjustment of Red/Pr / G/Y / B/Pb channel gain (contrast). Need to decreased with certain sources with higher than nominal video levels (e.g. 1-CHIP SNES consoles) to avoid clipping
</p>
<ul><li> <b>0-15</b>: <b>[default=8]</b>
</li></ul>
<h3> <span class="mw-headline" id="Sampling_opt."> Sampling opt. </span></h3>
<h4> <span class="mw-headline" id="480p_in_sampler"> 480p in sampler </span></h4>
<p><i>Controls the sampling mode when 525-line progressive signal (“480p”) is detected at input</i>
</p>
<ul><li> <b>Auto</b>: “VGA 640x480”-mode is selected when the signal comes from RGBHV input. “DTV 480p”-mode is selected with all other inputs <b>[default]</b>
</li><li> <b>DTV 480p</b>: Input is sampled at 858 samples per line, typically associated with 720x480 mode (CEA-861 spec.) used by DTV/DVD equipment and newer game consoles. This option forces the sampling mode for all inputs, which may be required for optimal image quality when e.g. Dreamcast with a VGA module is connected to RGBHV input.
</li><li> <b>VESA 640x480@60</b>: Input is sampled at 800 samples per line, typically associated with VESA 640x480@60Hz mode used by PCs. This option forces the sampling mode for all inputs.
</li></ul>
<h4> <span class="mw-headline" id="400p_in_sampler"> 400p in sampler </span></h4>
<p><i>Controls the sampling mode when 449-line progressive signal (“400p”) is detected at input</i>
</p>
<ul><li> <b>VGA 640x400@70</b>: Input is sampled at 800 samples per line, typically associated with VGA Mode 13h <b>[default]</b>
</li><li> <b>VGA 720x400@70</b>: Input is sampled at 900 samples per line, typically associated with VGA Mode 3+/7+
</li></ul>
<h4> <span class="mw-headline" id="Allow_TVP_HPLL2x"> Allow TVP HPLL2x </span></h4>
<p><i>Controls whether video digitizer H-PLL uses 2x sampling clock internally on supported video modes.</i>
</p>
<ul><li> <b>On</b>: Enables 2x H-PLL, generally reducing jitter at the price of inaccurate sampling phase due to internal bug. <b>[default]</b>
</li><li> <b>Off</b>: Disables 2x H-PLL, which might help with Line5x stability.
</li></ul>
<h4> <span class="mw-headline" id="Allow_upsample2x"> Allow upsample2x </span></h4>
<p><i>Controls whether 2x samplerate is used instead of pixel repetition in certain modes, e.g. 384pX2, 480pX2, 480iX3, 480iX4, 960iX2.</i>
</p>
<ul><li> <b>On</b>: 2x samplerate is used to double output horizontal resolution, which may be useful with sources that use off-spec horizontal rate. Alternatively, the option can be used to generate slightly more analog-esque (i.e. less pixellated) picture.
</li><li> <b>Off</b>: Pixel repetition is used to double output horizontal resolution, which regenerates source image most faithfully if sampling matches dot clock. <b>[default]</b>
</li></ul>
<h4> <span class="mw-headline" id="Advanced_timing_tweaker"> Advanced timing tweaker </span></h4>
<p><i>Allows fine-tuning of sampling/output parameters. Results greatly depend on displays - generally only position (backporch) adjustments are highly compatible. Efficient use requires knowledge of input and output hardware connected to OSSC. Video mode to edit (default is current mode) is selected via LEFT/RIGHT keys, after which tweaker is accessed via OK key. For more information, see the link below.</i>
</p><p><a href="/xrgb/index.php?title=Optimal_timings" title="Optimal timings">Optimal timings</a>
</p>
<h5> <span class="mw-headline" id="Horizontal_samplerate"> Horizontal samplerate </span></h5>
<p><i>Sets how many samples ADC take each scanline (=between 2 hsync signals). Mainly usable for console-specific fine-tuning in 320x240 / 256x240 optim. modes.</i>
</p>
<h5> <span class="mw-headline" id="H._s.rate_adj"> H. s.rate adj </span></h5>
<p><i>Fine-tune fractional H.samplerate adjustment for optimized modes. Value set is a target - closest effective value is automatically selected since actual samplerate resolution (between 1/6 and 1) depends on line multiplication mode.</i>
</p>
<h5> <span class="mw-headline" id="Horizontal.2FVertical_sync_length"> Horizontal/Vertical sync length </span></h5>
<p><i>Sets output sync lengths, which by default are set to match expected input sync lengths. Usually no need to modify.</i>
</p>
<h5> <span class="mw-headline" id="Horizontal.2FVertical_backporch_length"> Horizontal/Vertical backporch length </span></h5>
<p><i>Sets output backporch lengths, which by default are set to match expected input backporch lengths. Effectively adjusts image position.</i>
</p>
<h5> <span class="mw-headline" id="Horizontal.2FVertical_active_length"> Horizontal/Vertical active length </span></h5>
<p><i>Sets the area which is marked as active in output signal. Enables image size adjustments on compatible displays.</i>
</p>
<h5> <span class="mw-headline" id="Sampling_phase"> Sampling phase </span></h5>
<ul><li> <b>0-347 deg</b>: Selects the phase of regenerated pixel clock (=position where each sample is taken). When output rate matches the input DAC rate (PC graphics modes, newer consoles, 2 last linetriple modes), it is important to adjust sampling phase for optimal quality. This setting should be adjusted only after adjusting sync and video LPF since they can alter the relative position of video and sync signals. Can be also adjusted with remote hotkeys while tweaking other sampling settings <b>[default=180deg]</b>
</li></ul>
<h3> <span class="mw-headline" id="Sync_opt."> Sync opt. </span></h3>
<h4> <span class="mw-headline" id="Analog_sync_LPF"> Analog sync LPF </span></h4>
<p><i>Low-pass filter selection for analog sync signals (SCART and component inputs plus VGA input in RGsB mode). Required if there is noise or glitches on the sync line.</i>
</p>
<ul><li> <b>2.5MHz</b>: Highest filtering – recommended for sources that do not provide clean sync. <b>[default]</b>
</li><li> <b>10MHz</b>: Medium filtering.
</li><li> <b>33MHz</b>: Lowest filtering.
</li><li> <b>Off</b>: Sync is not filtered before processing.
</li></ul>
<h4> <span class="mw-headline" id="Analog_sync_Vth"> Analog sync Vth </span></h4>
<p><i>Sets the sync slicer threshold. May help with dropouts as the last resort - sync LPF and coast settings should be tested through first.</i>
</p>
<ul><li> <b>0-350mV</b>: threshold voltage. <b>[default=124mV]</b>
</li></ul>
<h4> <span class="mw-headline" id="Hsync_tolerance"> Hsync tolerance </span></h4>
<p><i>Sets tolerance for hsync period variation outside of vsync. Needs to be increased from default to allow detection of some consoles like certain Neo Geo models. H-PLL coast also needs to be increased to enable stable output with these problematic sources.</i>
</p>
<ul><li> <b>0-39.2us</b>: max. allowed period variance. <b>[default=0.92us]</b>
</li></ul>
<h4> <span class="mw-headline" id="Vsync_threshold"> Vsync threshold </span></h4>
<p><i>Sets delay threshold for extracting vsync from csync. The value should be higher than hsync length but lower that actual vsync length. Useful setting for Taito F2/F3 arcade boards</i>
</p>
<ul><li> <b>1.5-30.7us</b>: delay threshold. <b>[default=10.4us]</b>
</li></ul>
<h4> <span class="mw-headline" id="H-PLL_Pre-Coast"> H-PLL Pre-Coast </span></h4>
<p><i>Defines when PLL coast (current freq. freeze) is activated. Higher than default value needed with some sources (e.g. MD) for stable sync.</i>
</p>
<ul><li> <b>0-5 lines</b>: Number of scanlines before vsync at when coast is activated. <b>[default=1]</b>
</li></ul>
<h4> <span class="mw-headline" id="H-PLL_Post-Coast"> H-PLL Post-Coast </span></h4>
<p><i>Defines when PLL coast (current freq. freeze) is deactivated. Higher than default value needed with some sources (e.g. MD) for stable sync.</i>
</p>
<ul><li> <b>0-5 lines</b>: Number of scanlines after vsync at when coast is deactivated. <b>[default=0]</b>
</li></ul>
<h3> <span class="mw-headline" id="Output_opt."> Output opt. </span></h3>
<h4> <span class="mw-headline" id="240p.2F288p_proc"> 240p/288p proc </span></h4>
<p><i>Controls line multiplication setting for 240p/288p modes. NOTE: 3x/4x/5x do not generate standard 720p/960p/1080p/1200p CEA/VESA modes (total lines, pixels per line), so they are generally accepted only by monitors and not by many consumer TVs.</i>
</p>
<ul><li> <b>Passthru</b>: Only digitization is applied
</li><li> <b>Line2x</b>: Linedoubled 480p output. <b>[default]</b>
</li><li> <b>Line3x</b>: Linetripled 720p output.
</li><li> <b>Line4x</b>: 960p output.
</li><li> <b>Line5x</b>: 1080p/1200p output depending on <i>Line5x format</i> setting
</li></ul>
<h4> <span class="mw-headline" id="384p.2F400p_proc"> 384p/400p proc </span></h4>
<p><i>Controls line multiplication setting for 384p/400p modes</i>
</p>
<ul><li> <b>Passthru</b>: Only digitization is applied
</li><li> <b>Line2x</b>: Linedoubled 1024x768 output. <b>[default]</b>
</li><li> <b>Line2x 240x360</b>: Linedoubled 720p output mainly targeted for GBI
</li><li> <b>Line3x 240x360</b>: Linetripled 1080p output mainly targeted for GBI
</li><li> <b>Line3x Generic</b>: 1600x1200 mode for 400p input. Not guaranteed to work due to pixel clock exceeding recommended HW limits
</li></ul>
<h4> <span class="mw-headline" id="480i.2F576i_proc"> 480i/576i proc </span></h4>
<p><i>Controls line multiplication setting for 480i/576i modes</i>
</p>
<ul><li> <b>Passthru</b>: Only digitization is applied, deinterlacing will be handled by display. Generally results to higher quality picture at the price of added latency.
</li><li> <b>Line2x (bob)</b>: Linedoubled 480p/576p output. <b>[default]</b>
</li><li> <b>Line3x (laced)</b>: Linetripled 1440i/1728i output.
</li><li> <b>Line4x (bob)</b>: Linequadrupled 960p/1152p output.
</li></ul>
<p><b>Beware of using the OSSCs Line2x (bob) or Line4x (bob) deinterlacing modes on sources that display static graphics or text for a long period of time.</b> The OSSCs deinterlacer produces a constant flickering effect. This can cause image retention/burn in to occur faster than normal.
</p>
<h4> <span class="mw-headline" id="480p.2F576p_proc"> 480p/576p proc </span></h4>
<p><i>Controls line multiplication setting for 480p/576p modes</i>
</p>
<ul><li> <b>Passthru</b>: Only digitization is applied. <b>[default]</b>
</li><li> <b>Line2x</b>: Linedoubled 960p/1152p output. 
</li></ul>
<h4> <span class="mw-headline" id="960i.2F1080i_proc"> 960i/1080i proc </span></h4>
<p><i>Controls line multiplication setting for 960i/1080i modes</i>
</p>
<ul><li> <b>Passthru</b>: Only digitization is applied, deinterlacing will be handled by display. Generally results to higher quality picture at the price of added latency.
</li><li> <b>Line2x (bob)</b>: Linedoubled 1280x960/1920x1080 output. <b>[default]</b>
</li></ul>
<p><b>Beware of using the OSSCs Line2x (bob) deinterlacing mode on sources that display static graphics or text for a long period of time.</b> The OSSCs deinterlacer produces a constant flickering effect. This can cause image retention/burn in to occur faster than normal.
</p>
<h4> <span class="mw-headline" id="Line2x_mode"> Line2x mode </span></h4>
<p><i>Controls the sampling and pixel clock multiplication mode for line2x.</i>
</p>
<ul><li> <b>Generic 4:3</b>: Uses full horizontal sample rate without pixel multiplication, resulting to 720x480/576 output (4:3 aspect). <b>[default]</b>
</li><li> <b>512x240 optim.</b>: For advanced users only - requires clock and phase adjustments. Uses a sampling rate which matches the DAC rate of 682 dots per line used by some classic consoles (e.g. SNES hi-res) in 512 mode, resulting to pixel-perfect digitization. Output is pixel-multiplied by 2 in horizontal direction, resulting to 1024x480 effective area of 1024x480 output. Note: If picture jitters when this mode is selected, adjust sampling phase until sweet spot is achieved.
</li><li> <b>384x240 optim.</b>: For advanced users only - requires clock and phase adjustments. Uses a sampling rate which matches the DAC rate of 512 dots per line used by some systems (e.g. CPS2) in 384x240 mode, resulting to pixel-perfect digitization.
</li><li> <b>320x240 optim.</b>: For advanced users only - requires clock and phase adjustments. Uses a sampling rate which matches the DAC rate of 426 dots per line used by some classic consoles (e.g. several PSX games) in 320x240 mode, resulting to pixel-perfect digitization. Output is pixel-multiplied by 2 in horizontal direction, resulting to 640x480 effective area of 640x480 output. Note: If picture jitters when this mode is selected, adjust sampling phase until sweet spot is achieved.
</li><li> <b>256x240 optim.</b>: For advanced users only - requires clock and phase adjustments. Uses a sampling rate which matches the DAC rate of 341 dots per line used by various classic consoles (e.g. NES, SNES) in 256x240 mode, resulting to pixel-perfect digitization. Output is pixel-multiplied in horizontal direction, resulting to 768x480 or 512x480 (depending on <i>256x240 aspect</i> setting) effective area of 768x480 output. Note: If picture jitters when this mode is selected, adjust sampling phase until sweet spot is achieved.
</li></ul>
<h4> <span class="mw-headline" id="Line3x_mode"> Line3x mode </span></h4>
<p><i>Controls the sampling and pixel clock multiplication mode for line3x.</i>
</p>
<ul><li> <b>Generic 16:9</b>: Uses full horizontal sample rate without pixel multiplication, resulting to fully utilized 1280x720/864 output (16:9 aspect). Useful if connected to a CRT via DVI-&gt;VGA converter.
</li><li> <b>Generic 4:3</b>: Uses 3/4 of full horizontal sample rate without pixel multiplication, resulting to 960x720/864 effective area of 1280x720/864 output (4:3 aspect). <b>[default]</b>
</li><li> <b>512x240 optim.</b>: For advanced users only - requires clock and phase adjustments. Uses a sampling rate which matches the DAC rate of 682 dots per line used by some classic consoles (e.g. SNES hi-res) in 512 mode, resulting to pixel-perfect digitization. Output is pixel-multiplied by 2 in horizontal direction, resulting to 1024x720 effective area of 1024x720 output. Note: If picture jitters when this mode is selected, adjust sampling phase until sweet spot is achieved.
</li><li> <b>384x240 optim.</b>: For advanced users only - requires clock and phase adjustments. Uses a sampling rate which matches the DAC rate of 512 dots per line used by some systems (e.g. CPS2) in 384x240 mode, resulting to pixel-perfect digitization.
</li><li> <b>320x240 optim.</b>: For advanced users only - requires clock and phase adjustments. Uses a sampling rate which matches the DAC rate of 426 dots per line used by some classic consoles (e.g. several PSX games) in 320x240 mode, resulting to pixel-perfect digitization. Output is pixel-multiplied by 3 in horizontal direction, resulting to 960x720 effective area of 1280x720 output. Note: If picture jitters when this mode is selected, adjust sampling phase until sweet spot is achieved.
</li><li> <b>256x240 optim.</b>: For advanced users only - requires clock and phase adjustments. Uses a sampling rate which matches the DAC rate of 341 dots per line used by various classic consoles (e.g. NES, SNES) in 256x240 mode, resulting to pixel-perfect digitization. Output is pixel-multiplied in horizontal direction, resulting to 1024x720 or 768x720 (depending on <i>256x240 aspect</i> setting) effective area of 1280x720 output. Note: If picture jitters when this mode is selected, adjust sampling phase until sweet spot is achieved.
</li></ul>
<h4> <span class="mw-headline" id="Line4x_mode"> Line4x mode </span></h4>
<p><i>Controls the sampling and pixel clock multiplication mode for line4x.</i>
</p>
<ul><li> <b>Generic 4:3</b>: Uses full horizontal sample rate without pixel multiplication, resulting to 1280x960/1152 output (4:3 aspect). <b>[default]</b>
</li><li> <b>512x240 optim.</b>: For advanced users only - requires clock and phase adjustments. Uses a sampling rate which matches the DAC rate of 682 dots per line used by some classic consoles (e.g. SNES hi-res) in 512 mode, resulting to pixel-perfect digitization. Output is pixel-multiplied by 2 in horizontal direction, resulting to 1024x960 effective area of 1024x960 output. Note: If picture jitters when this mode is selected, adjust sampling phase until sweet spot is achieved.
</li><li> <b>384x240 optim.</b>: For advanced users only - requires clock and phase adjustments. Uses a sampling rate which matches the DAC rate of 512 dots per line used by some systems (e.g. CPS2) in 384x240 mode, resulting to pixel-perfect digitization.
</li><li> <b>320x240 optim.</b>: For advanced users only - requires clock and phase adjustments. Uses a sampling rate which matches the DAC rate of 426 dots per line used by some classic consoles (e.g. several PSX games) in 320x240 mode, resulting to pixel-perfect digitization. Output is pixel-multiplied by 4 in horizontal direction, resulting to 1280x960 effective area of 1280x960 output. Note: If picture jitters when this mode is selected, adjust sampling phase until sweet spot is achieved.
</li><li> <b>256x240 optim.</b>: For advanced users only - requires clock and phase adjustments. Uses a sampling rate which matches the DAC rate of 341 dots per line used by various classic consoles (e.g. NES, SNES) in 256x240 mode, resulting to pixel-perfect digitization. Output is pixel-multiplied in horizontal direction, resulting to 1280x960 or 1024x960 (depending on <i>256x240 aspect</i> setting) effective area of 1280x960 output. Note: If picture jitters when this mode is selected, adjust sampling phase until sweet spot is achieved.
</li></ul>
<h4> <span class="mw-headline" id="Line5x_mode"> Line5x mode </span></h4>
<p><i>Controls the sampling and pixel clock multiplication mode for line5x.</i>
</p>
<ul><li> <b>Generic 4:3</b>: Uses full horizontal sample rate without pixel multiplication, resulting to 1600x1080/1200 output (4:3 aspect). <b>[default]</b>
</li><li> <b>512x240 optim.</b>: For advanced users only - requires clock and phase adjustments. Uses a sampling rate which matches the DAC rate of 682 dots per line used by some classic consoles (e.g. SNES hi-res) in 512 mode, resulting to pixel-perfect digitization. Output is pixel-multiplied by 3 in horizontal direction, resulting to 1536x1080/1200 effective area of 1080p/1200p output. Note: If picture jitters when this mode is selected, adjust sampling phase until sweet spot is achieved.
</li><li> <b>384x240 optim.</b>: For advanced users only - requires clock and phase adjustments. Uses a sampling rate which matches the DAC rate of 512 dots per line used by some systems (e.g. CPS2) in 384x240 mode, resulting to pixel-perfect digitization.
</li><li> <b>320x240 optim.</b>: For advanced users only - requires clock and phase adjustments. Uses a sampling rate which matches the DAC rate of 426 dots per line used by some classic consoles (e.g. several PSX games) in 320x240 mode, resulting to pixel-perfect digitization. Output is pixel-multiplied by 5 in horizontal direction, resulting to 1600x1080/1200 effective area of 1080p/1200p output. Note: If picture jitters when this mode is selected, adjust sampling phase until sweet spot is achieved.
</li><li> <b>256x240 optim.</b>: For advanced users only - requires clock and phase adjustments. Uses a sampling rate which matches the DAC rate of 341 dots per line used by various classic consoles (e.g. NES, SNES) in 256x240 mode, resulting to pixel-perfect digitization. Output is pixel-multiplied in horizontal direction, resulting to 1536x1080/1200 or 1280x1080/1200 (depending on <i>256x240 aspect</i> setting) effective area of 1080p/1200p output. Note: If picture jitters when this mode is selected, adjust sampling phase until sweet spot is achieved.
</li></ul>
<p>Using properly rated HDMI/DVI cables for Line5x mode is essential. Note that this mode is also incompatible with certain HDMI splitters. For some devices/displays, tweaking of the advanced timing options may be necessary. For example, on the VP50 Pro video processor, you should use H. Samplerate 2057 and H. Backporch 255 on the OSSC.
</p>
<h4> <span class="mw-headline" id="Line5x_format"> Line5x format </span></h4>
<p><i>Selects the output format of line5x.</i>
</p>
<ul><li> <b>1920x1080</b>: 1080-line output, which crops a few active lines from top and bottom of incoming video signal. <b>[default]</b>
</li><li> <b>1600x1200</b>: 1200-line output that displays all active lines of incoming video signal.
</li><li> <b>1920x1200</b>: 1200-line output that displays all active lines of incoming video signal.
</li></ul>
<p>Note - When using Line 5x mode, if your display can tolerate it, adjust h.samplerate to 1950 using the <a rel="nofollow" class="external text" href="http://junkerhq.net/xrgb/index.php?title=OSSC#Advanced_timing_tweaker">Advanced Timing Tweaker</a>. This will help correct the image aspect ratio.
</p>
<h4> <span class="mw-headline" id="256x240_aspect"> 256x240 aspect </span></h4>
<p><i>Selects the output aspect for 256x240 optim. mode.</i>
</p>
<ul><li> <b>4:3</b>: Integer-multiplication is handled so that target aspect is close to 4:3. <b>[default]</b>
</li><li> <b>8:7</b>: Maintains square pixel aspect ratio.
</li></ul>
<h4> <span class="mw-headline" id="TX_mode"> TX mode </span></h4>
<p><i>Sets the output TX mode.</i>
</p>
<ul><li> <b>HDMI (RGB)</b>: 24-bit full-range RGB output with audio and auxiliary Infoframe packets. <b>[default for v1.6 and DIY boards]</b>
</li><li> <b>HDMI (YCbCr444)</b>: 24-bit YCbCr 4:4:4 (Rec. 601) output with audio and auxiliary Infoframe packets. Recommended for displays which do not support RGB in full-range.
</li><li> <b>DVI</b>: 24-bit full-range RGB output. Required if target display does not support HDMI. <b>[default for DVI boards]</b>
</li></ul>
<h4> <span class="mw-headline" id="HDMI_ITC"> HDMI ITC </span></h4>
<p><i>Sets IT content flag in AVI Infoframe when in HDMI TX mode.</i>
</p>
<ul><li> <b>Off</b>: No indication about content type. <b>[default]</b>
</li><li> <b>On</b>: Output is flagged as IT Content, hinting the dispaly that video filtering should not be applied and that source is in sRGB color space (and in full-range format). May reduce delay or change picture processing on certain displays.
</li></ul>
<h3> <span class="mw-headline" id="Scanline_opt."> Scanline opt. </span></h3>
<h4> <span class="mw-headline" id="Scanlines"> Scanlines </span></h4>
<p><i>Controls whether emulated scanlines are drawn on top of the picture</i> 
</p>
<ul><li> <b>Off</b>: No scanlines drawn <b>[default]</b>
</li><li> <b>Auto</b>: Horizontal scanlines are drawn for 240p/288p sources, alternating scanlines are enabled for 480i/576i, no scanlines for other sources
</li><li> <b>On</b>: Scanlines are drawn for every source according to "Scanline type" option
</li></ul>
<h4> <span class="mw-headline" id="Sl._strength"> Sl. strength </span></h4>
<ul><li> <b>6-100%</b>: Strength of the emulated scanlines <b>[default=6%]</b>
</li></ul>
<h4> <span class="mw-headline" id="Sl._hybrid_str"> Sl. hybrid str </span></h4>
<ul><li> <b>0-175%</b>: Strength of hybrid/blend effect (depedence of the pixel that is overlayed) in scanlines <b>[default=0%]</b>
</li></ul>
<h4> <span class="mw-headline" id="Sl._method"> Sl. method </span></h4>
<p><i>Selects the method how scanlines are generated</i> 
</p>
<ul><li> <b>Multiplication</b>: Scanline is generated by multiplying source RGB value <b>[default]</b>
</li><li> <b>Subtraction</b>: Scanline is generated by subtracting from source RGB value
</li></ul>
<h4> <span class="mw-headline" id="Sl._alternating"> Sl. alternating </span></h4>
<p><i>Controls whether scanline position alternates along with fields of interlaced sources</i>
</p>
<ul><li> <b>Off</b>: Scanlines are always mapped to same output lines.
</li><li> <b>On</b>: Position is tied to field which shows as alternating position in output. Useful for reducing flicker. <b>[default]</b>
</li></ul>
<h4> <span class="mw-headline" id="Sl._alignment"> Sl. alignment </span></h4>
<ul><li> <b>Top</b>: Scanline is drawn on top position of every group of output lines formed from a single input line. <b>[default]</b>
</li><li> <b>Bottom</b>: Scanline is drawn on bottom position of every group of output lines formed from a single input line.
</li></ul>
<h4> <span class="mw-headline" id="Sl._alt_interval"> Sl. alt interval </span></h4>
<p><i>Controls whether scanlines are drawn at alternative interval</i> 
</p>
<ul><li> <b>Off</b>: Standard interval is used. <b>[default]</b>
</li><li> <b>On</b>: Scanline overlay is drawn on top on every other input line. Useful for sources which are pre-linemultiplied and then further multiplied by OSSC.
</li></ul>
<h4> <span class="mw-headline" id="Scanline_type"> Scanline type </span></h4>
<ul><li> <b>Horizontal</b>: Scanlines are drawn on every other (passthru &amp; line2x modes), every third (line3x), every 2 out of 4 (line4x) or every 2 out of 5 (line5x) output lines. <b>[default]</b>
</li><li> <b>Vertical</b>: Scanlines are drawn on every other output column.
</li><li> <b>Horiz. + Vert.</b>: Combination of horizontal and vertical mode.
</li><li> <b>Custom</b>: Scanlines are drawn accoring to line-wise and column-wise strength set under Custom Sl.
</li></ul>
<h4> <span class="mw-headline" id="Custom_Sl."> Custom Sl. </span></h4>
<p><i>Enables separate setting of each overlay line and column (line strength takes priority on pixels where it is &gt;0%). To check how many sub-lines and -columns are in each mode, refer to <a href="/xrgb/index.php?title=Optimal_timings#Horizontal_multiplication_factors" title="Optimal timings">Optimal timings#Horizontal multiplication factors</a>.</i> 
</p>
<h5> <span class="mw-headline" id="Sub-line_M_str"> Sub-line M str </span></h5>
<p><i>Strength for Mth sub-line, 0% disables line overlay.</i>
</p>
<h5> <span class="mw-headline" id="Sub-column_N_str"> Sub-column N str </span></h5>
<p><i>Strength for Nth sub-column, 0% disables column overlay.</i>
</p>
<h3> <span class="mw-headline" id="Post-proc."> Post-proc. </span></h3>
<h4> <span class="mw-headline" id="Horizontal_mask"> Horizontal mask </span></h4>
<ul><li> <b>0-255 pixels</b>: Controls the size of a mask (black border) generated around the picture in horizontal direction (1-pixel steps). Can be used to mask areas which would get hidden in the overscan region of CRT TVs. <b>[default=0]</b>
</li></ul>
<h4> <span class="mw-headline" id="Vertical_mask"> Vertical mask </span></h4>
<ul><li> <b>0-63 pixels</b>: Controls the size of a mask (black border) generated around the picture in vertical direction (1-pixel steps). Can be used to mask areas which would get hidden in the overscan region of CRT TVs. <b>[default=0]</b>
</li></ul>
<h4> <span class="mw-headline" id="Mask_brightness"> Mask brightness </span></h4>
<p><i>Sets output aspect brightness. Could be used as a precaution with self-emissive displays to avoid uneven wear.</i>
</p>
<ul><li> <b>0-15</b>: Mask brightness level. <b>[default=0]</b>
</li></ul>
<h4> <span class="mw-headline" id="Reverse_LPF"> Reverse LPF </span></h4>
<p><i>Compensates unintended LPF/bleeding caused by sub-optimal video DAC (e.g. 1st rev SNES consoles) or long cables.</i>
</p>
<ul><li> <b>0-31</b>: Reverse LPF strength. <b>[default=0]</b>
</li></ul>
<h4> <span class="mw-headline" id="DIY_latency_tester"> DIY latency tester </span></h4>
<p><a href="/xrgb/index.php?title=OSSC_latency_tester" title="OSSC latency tester">OSSC latency tester</a>
</p>
<h3> <span class="mw-headline" id="Compatibility"> Compatibility </span></h3>
<p>Options that may need to be set to achieve compatibility with certain sources / displays. <b>Do not enable unless absolutely required</b>, since they come with downsides.
</p>
<h4> <span class="mw-headline" id="Full_TX_setup"> Full TX setup </span></h4>
<p><i>Sets whether TX initialization is done every time a video mode changes.</i>
</p>
<ul><li> <b>Off</b>: TX is kept on during mode changes. <b>[default]</b>
</li><li> <b>On</b>: TX is reinitialized when input/output mode changes, resulting to a short blank. Needed if display permanently loses sync / picture position during video mode changes.
</li></ul>
<h4> <span class="mw-headline" id="AV3_interlacefix"> AV3 interlacefix </span></h4>
<p><i>Sets whether internal sampling rate is kept minimal with 480i/576i modes.</i>
</p>
<ul><li> <b>Off</b>: Internal sampling rate of 480i/576i is doubled to minimize jitter and generate optimal pclk input for FPGA PLL. <b>[default]</b>
</li><li> <b>On</b>: Internal sampling rate of 480i/576i is not doubled, improving interlace detection via AV3 when sync edges are not perfectly aligned.
</li></ul>
<h4> <span class="mw-headline" id="AV3_use_AV1_RGB"> AV3 use AV1 RGB </span></h4>
<p><i>Selects whether AV1 RGB and audio inputs are used with AV3 RGBHV and RGBS modes. Together with a small <a href="/xrgb/index.php?title=OSSC_AV3_use_AV1_RGB_mod" title="OSSC AV3 use AV1 RGB mod">HW modification</a>, Taito F3 etc. problematic systems can be connected to AV1.</i>
</p>
<ul><li> <b>Off</b>: AV3 mode uses AV3 RGB and audio inputs. <b>[default]</b>
</li><li> <b>On</b>: AV3 mode uses AV1 RGB and audio inputs.
</li></ul>
<h4> <span class="mw-headline" id="Default_HDMI_VIC"> Default HDMI VIC </span></h4>
<p><i>Selects Video Format Identification Code (VIC) which is indicated on HDMI AVI Infoframe for preset modes which do not have VIC specificed. Can be used to work around devices (switches/displays) that do not accept default VIC (0) indicating unknown mode.</i>
</p>
<ul><li> <b>0-31</b>: VIC value. Try setting 2 (480p60) with problematic sinks. <b>[default=0]</b>
</li></ul>
<h4> <span class="mw-headline" id="Panasonic_hack"> Panasonic hack </span></h4>
<p><i>Signal hack which improves line count tolerance with certain Panasonic TVs. Useful for Neo-Geo and PSX 288p in line2x mode.</i>
</p>
<ul><li> <b>Off</b>: Disabled.<b>[default]</b>
</li><li> <b>On</b>: Data enable signal is cut short on last active line in line2x mode.
</li></ul>
<h3> <span class="mw-headline" id="Audio_options_.28available_in_-aud_firmware.29"> Audio options (available in <i>-aud</i> firmware) </span></h3>
<h4> <span class="mw-headline" id="Down-sampling"> Down-sampling </span></h4>
<ul><li> <b>2x  (fs = 48kHz)</b>: Downsample 24bit/96kHz audio signal from audio ACD to 24bit/48kHz for best compatibility. <b>[default]</b>
</li><li> <b>Off (fs = 96kHz)</b>: Do not downsample digitized audio signal.
</li></ul>
<h4> <span class="mw-headline" id="Swap_left.2Fright"> Swap left/right </span></h4>
<ul><li> <b>Off</b>: Do not swap audio channels. <b>[default]</b>
</li><li> <b>On</b>: Swap left/right audio channels.
</li></ul>
<h4> <span class="mw-headline" id="Pre-ADC_gain_2"> Pre-ADC gain </span></h4>
<p><i>Volume gain adjustment before audio is digitized. Can be used to compensate level differences between sources.</i>
</p>
<ul><li> <b>-12-+12dB</b>: Gain. <b>[default=0dB]</b>
</li></ul>
<h3> <span class="mw-headline" id="Settings_opt."> Settings opt. </span></h3>
<p>Global settings (not part of profile, but saved when a profile is saved/loaded)
</p>
<h4> <span class="mw-headline" id="Load_profile"> Load profile </span></h4>
<p><i>Loads profile-specific settings (including adv. timing parameters) from a selected profile slot (0-9). This profile slot will be subsequently loaded on startup.</i>
</p>
<h4> <span class="mw-headline" id="Save_profile"> Save profile </span></h4>
<p><i>Saves profile-specific settings (including adv. timing parameters) to a selected profile slot (0-9). This profile slot will be subsequently loaded on startup.</i>
</p>
<h4> <span class="mw-headline" id="Reset_settings"> Reset settings </span></h4>
<p><i>Resets current profile to default values without saving it.</i>
</p>
<h4> <span class="mw-headline" id="Link_prof-.3Einput"> Link prof-&gt;input </span></h4>
<p><i>A target input can be set for current profile. Any time the profile is manually loaded, corresponding input is selected automatically.</i>
</p>
<h4> <span class="mw-headline" id="Link_input-.3Eprof"> Link input-&gt;prof </span></h4>
<p><i>When enabled, each logical input tracks which profile was used last and it is automatically loaded when input is selected manually.</i>
</p>
<h4> <span class="mw-headline" id="Initial_input"> Initial input </span></h4>
<p><i>Sets the input which is automatically activated when device is powered on. If "last used" is selected, id is saved every time input is switched (adding a minor delay) and is automatically selected next time OSSC is powered on. Test pattern is diplayed regardless of initial input setting until sync is detected on the respective input.</i>
</p>
<h4> <span class="mw-headline" id="Autodetect_input"> Autodetect input </span></h4>
<p><i>Selects whether inputs are scanned to automatically detect active source. Scanning continues until sync is detected or timeout is met. Scanning can be (re)started by pressing RIGHT on the remote.</i>
</p>
<ul><li> <b>Off</b>: Do not autodetect source. <b>[default]</b>
</li><li> <b>Current input</b>: Scan different input modes on current physical input to autodetect source.
</li><li> <b>All inputs</b>: Scan different input modes across all physical inputs to autodetect source.
</li></ul>
<h4> <span class="mw-headline" id="Auto_AV1_Y.2FGs"> Auto AV1 Y/Gs </span></h4>
<p>Selects whether automatic input detection should select RGsB or YPbPr mode when sync is detected on Y/Gs line on AV1.
</p>
<ul><li> <b>RGsB</b>: RGsB mode is selected. <b>[default]</b>
</li><li> <b>YPbPr</b>: YPbPr mode is selected.
</li></ul>
<h4> <span class="mw-headline" id="Auto_AV2_Y.2FGs"> Auto AV2 Y/Gs </span></h4>
<p>Selects whether automatic input detection should select RGsB or YPbPr mode when sync is detected on Y/Gs line on AV2.
</p>
<ul><li> <b>RGsB</b>: RGsB mode is selected.
</li><li> <b>YPbPr</b>: YPbPr mode is selected. <b>[default]</b>
</li></ul>
<h4> <span class="mw-headline" id="Auto_AV3_Y.2FGs"> Auto AV3 Y/Gs </span></h4>
<p>Selects whether automatic input detection should select RGsB or YPbPr mode when sync is detected on Y/Gs line on AV3.
</p>
<ul><li> <b>RGsB</b>: RGsB mode is selected. <b>[default]</b>
</li><li> <b>YPbPr</b>: YPbPr mode is selected.
</li></ul>
<h4> <span class="mw-headline" id="LCD_BL_timeout"> LCD BL timeout </span></h4>
<p><i>Sets backlight timeout for on-board character LCD. When enabled, backlight is automatically is turned off automatically when in main screen and no input from user has received for the set time</i>
</p>
<h4> <span class="mw-headline" id="Import_settings"> Import settings </span></h4>
<p>Imports profiles made using <a rel="nofollow" class="external text" href="http://pbnl.byethost7.com/ossc/profiles/">this</a> web app which are stored on a SD card.
</p>
<h4> <span class="mw-headline" id="Fw._update"> Fw. update </span></h4>
<p>See the dedicated section on the bottom.
</p>
<h2> <span class="mw-headline" id="Compatibility_and_special_configuration"> Compatibility and special configuration </span></h2>
<p>We encourage the community to add sections under each system instead of having an enormous table here. That way we can have more detailed and specific information on a per system basis, and here links to all the systems tested so far. A link to a summary page of potentially incompatible systems is found at the end of the list.
</p>

	

=======<BR>
For purchase OSSC visit my store http://www.manuferhi.com<BR>
For more information, contact with manuferhi@gmail.com






