# Time-lapse Setup

Start by connecting the camera via USB as described in the previous section.  This will enable the Time-lapse menu (the first item on the main screen).  Press the knob or enter button to select.  You'll then see the options listed in this section.

<aside class="notice">IMPORTANT: the camera must be in manual mode, set to capture in RAW (not RAW+JPEG)</aside>

### Quick Setup for the first test
For your first automatic ramping test, I recommend to start with the following configuration:

Setting | Recommended Value
------ | -------
Exposure | Just setup the camera for the current scene before hand and skip this step
Timelapse Mode | Auto Ramping
Interval Mode | Auto Variable
Day Interval | 8 seconds
Night Interval | 40 Seconds
Destination | Camera <sup>1</sup>

I recommend starting an hour before sunset, setting the camera at the lowest ISO, a moderately wide aperture (e.g., f/2.8) and then setting the shutter speed to whatever is needed for a good exposure (maybe 1/3200).  Make sure it's not overexposed!

Then, let it run at least 3 hours after sunset to get a good length and transition.  Or, if you have external power for the camera, go all night until sunrise!

To stop the time-lapse, press the menu (lower right) button while in the time-lapse status screen and then select "Stop Time-lapse".

Once the time-lapse is complete, check out the <a href="#post-processing">post-processing</a> section.

<sup>1</sup>This setting only appears if there is an SD card in the VIEW.  For older Sony cameras connected via USB, you'll need to set this to 'SD Card' and make sure an SD card is in the VIEW.  For other cameras, performance is best when saving directly to the camera.  Sony can save to the camera when connected via WiFi instead of USB (see <a href="#camera-specific-notes">camera-specific notes</a> for more).

### Time-lapse options are described below

## Exposure

Puts the camera in liveview mode for adjusting the exposure and focus. Press the menu (lower-right) button to cycle the selection between the settings shown below the image. Turn the knob to increase/decrease selected setting.

<aside class="notice">NOTE: the Exposure feature may not work well on all cameras.  If you have any trouble with it, simply adjust the exposure and focus on the camera before connecting the VIEW.</aside>

<aside class="success">Whether setup via the Exposure menu or in camera, the starting exposure for ramping is very important as it is used for a reference throughout the time-lapse.  Make sure it is not over-exposed, as excessively clipped (overexposed highlights) regions of the image can cause the exposure ramping to be inaccurate and make smoothing difficult in post-processing.</aside>

## Timelapse Mode

Option | Description
------ | -------
Fixed | This is for a basic time-lapse where the exposure and interval are constant throughout
Auto Ramping | In this mode the VIEW will automatically adjust the exposure to match changing light conditions

For short time-lapse clips during the day or night where the exposure and interval are constant, choose Fixed.

For sunsets, sunrises, day to night, night to day, and day to night to day, choose Auto Ramping.  This will also enable the Auto Interval options for interval ramping between day and night.

## Primary Camera

This option is only shown when more than one camera is connected to the VIEW.  The primary camera selection defines the camera used for setup and liveview, the status thumbnail, and the exposure tracking.  The settings from the primary camera are copied to all additional cameras connected, and they are triggered in sync.  This is nice for panoramas, as well as a wide view and a telephoto view for post-processing transitions.  In the case of wide and telephoto, make the wide view the primary for better exposure tracking.


## Interval Mode

This option is only shown when Timelapse Mode is set to 'Auto Ramping'

Option | Description
------ | -------
Fixed Length | This maintains the same interval through out the time-lapse and will limit the maximum shutter speed to fit within it
Auto Variable | This mode will automatically ramp between a Day Interval and a Night Interval and allows for longer shutter speeds at night
External AUX2 | Use this for synchronization with a motion system where the motion's camera trigger is connected to AUX2 and defines the interval (see <https://docs.view.tl/#external-trigger>)


## Interval

This option is only shown when Timelapse Mode is set to 'Fixed' or Interval Mode is set to 'Fixed'

Option | Description
------ | -------
[time in seconds] | Interval length in seconds.  This is the time between the start of one frame to the start of the next


## Frames

This option is only shown when Timelapse Mode is set to 'Fixed'. In Auto Ramping mode, the VIEW always runs until stopped.

Option | Description
------ | -------
[number of frames] | Number of exposures to complete before stopping


## Day Interval

This option is only shown when Timelapse Mode is set to 'Auto Ramping' and Interval Mode is set to 'Auto Variable'

This determines the interval length during daylight, based on the camera's exposure settings.  It will be smoothly ramped to/from the Night Interval as the ambient conditions (and camera exposure) change.

Option | Description
------ | -------
[time in seconds] | Interval length in seconds.  This is the time between the start of one frame to the start of the next


## Night Interval

This option is only shown when Timelapse Mode is set to 'Auto Ramping' and Interval Mode is set to 'Auto Variable'

This determines the interval length during the night, based on the camera's exposure settings.  It will be smoothly ramped to/from the Day Interval as the ambient conditions (and camera exposure) change.

Option | Description
------ | -------
[time in seconds] | Interval length in seconds.  This is the time between the start of one frame to the start of the next


## Ramping Options

This option is only shown when Timelapse Mode is set to 'Auto Ramping'.

In this menu, there are a few settings to configuring the limits of auto ramping.  Note that these options can limit the range of ramping and thereby cause it to not reach a proper exposure if too limited.  For most cameras, a max ISO of 6400 does well, with a lower ISO limit of 100 (best to only use native ISOs, not lower).

The Night Exposure setting defines how much less exposed "night" should be, relative to "day".  For example, a night exposure of -1 (the default), will underexposure a night scene by 1 stop compared to the day.  So, if an auto ramp is started during the day, and by night the exposure it too light, a lower night exposure is needed.  Or, if the images after sunset are too dark, a higher value should be used.  A Night Exposure setting of 0 will keep the day and night perceived luminosity the same.

Option | Description
------ | -------
Maximum ISO | Upper ISO limit for auto ramping
Minimum ISO | Lower ISO limit for auto ramping
Max Shutter | Longest shutter speed to use during ramping
Ramp Params | Which parameters to use for ramping <sup>1</sup>
Highlight Protection | When enabled, the VIEW will immediately decrease the exposure by 1/3 stop after each frame where excessive clipping is detected
Min Aperture | Minimum aperture to use for ramping, e.g., f2.8 (shown only if Ramp Params includes aperture)
Max Aperture | Maximum aperture to use for ramping, e.g., f11 (shown only if Ramp Params includes aperture)
Day Lum Target | Target image brightness for day exposure <sup>2</sup>
Night Lum Target | Target image brightness for day exposure <sup>2</sup>

<sup>1</sup> The "balanced" option tries to move shutter and ISO together, to more gradually increase the shutter speed.  The other settings always prioritize the lowest ISO possible.

<sup>2</sup> When starting during the day, the Day Lum Target is not used -- instead, the day brightness is based on the starting frame.  Likewise, when starting at night for a sunrise to day, the Night Lum Target is not used either -- only the day target.

Once the transition begins (sunrise or sunset) the VIEW switches between using the luminance of the starting frame as a target exposure and instead uses the Luminance Target of Night or Day, depending on which is approaching.  So once you've found night/day target values that you like, you don't have to change them.

The defaults are to have the Day Target at 0 -- meaning that to the VIEW the image seems to have a balanced exposure, and the Night Lum at -1.3, meaning that the exposure is about 1.3 stops less than balanced, giving the appearance of night.

If you did a night to day and thought the ending day exposure was about a stop too dark, increase the Day Lum Target to +1.  Keep in mind, however, it does run a little dark during sunrise to preserve colors and highlights and will brighten some after.


## Manual Aperture

This option is only shown when the aperture setting of the lens cannot be read from the camera, such as when using a manual lens or the lens-twist method.

Enter the aperture setting of the lens here to aid in the calculation of absolute exposure values to aid in day/night feathering of interval and exposure compensation.

Option | Description
------ | -------
[aperture] | Aperture value that the lens is set to or locked on (in the case of lens-twist)


## Destination

This option is only shown when an SD card is inserted in the VIEW.  Older Sony cameras require that the images be saved to the VIEW's SD card (<https://docs.view.tl/#sony-alpha-usb>), but otherwise it is recommended to only save to the camera's card

Option | Description
------ | -------
Camera | Keep images on the camera's card.  No SD card is needed in the VIEW.  This option is recommend for best performance. 
SD Card | Saves the time-lapse images in their own folder in the root of the SD card, along side the XMP files for Lightroom smoothing.

## START

If you have all the settings entered, select this option to start the time-lapse!  While it's running, press the enter (middle right) button or wave your hand to the right to review the results in process, or press the menu (lower right) button to stop the time-lapse.


To stop the time-lapse, press the menu (lower right) button while in the time-lapse status screen and then select "Stop Time-lapse".



