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
Destination | SD Card (you have to first put an SD card in the VIEW)

I recommend starting an hour before sunset, setting the camera at the lowest ISO, a moderately wide aperture (f/2.8) and then setting the shutter speed to whatever is needed for a good exposure (maybe 1/3200).  Make sure it's not overexposed!

Then, let it run at least 3 hours after sunset to get a good length and transition.  Or, if you have external power for the camera, go all night until sunrise!

### Time-lapse options are described below

## Exposure

Puts the camera in liveview mode for adjusting the exposure and focus. Turn the knob to increase/decrease exposure.  Press the enter button to toggle focus mode.  When in focus mode, the liveview image will be cropped to 100%, and the knob will then adjust focus rather than exposure.*


<aside class="notice">NOTE: the Exposure feature doesn't work on all cameras, particularly Sony.  In this case simply adjust the exposure and focus on the camera before connecting the VIEW.  Additionally, this mode is still in development -- if you have trouble, just setup the exposure in the camera.</aside>

<aside class="success">Whether setup via the Exposure menu or in camera, the starting exposure for ramping is very important as it is used for a reference throughout the time-lapse.  Make sure it is not over-exposed, as excessive clipped (overexposed highlights) regions of the image can cause the exposure ramping to be inaccurate.</aside>

## Timelapse Mode

Option | Description
------ | -------
Fixed | This is for a basic time-lapse where the exposure and interval are constant throughout
Auto Ramping | In this mode the VIEW will automatically adjust the exposure to match changing light conditions

For short time-lapse clips during the day or night where the exposure and interval are constant, choose Fixed.

For sunsets, sunrises, day to night, night to day, and day to night to day, choose Auto Ramping.  This will also enable the Auto Interval options for interval ramping between day and night.

## Interval Mode

This option is only shown when Timelapse Mode is set to 'Auto Ramping'

Option | Description
------ | -------
Fixed Length | This maintains the same interval through out the time-lapse and will limit the maximum shutter speed to fit within it
Auto Variable | This mode will automatically ramp between a Day Interval and a Night Interval and allows for longer shutter speeds at night


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
Night Exposure | Relative exposure difference for night vs. day
Maximum ISO | Upper ISO limit for auto ramping
Minimum ISO | Lower ISO limit for auto ramping
Max Shutter | Longest shutter speed to use during ramping


## Manual Aperture

This option is only shown when the aperture setting of the lens cannot be read from the camera, such as when using a manual lens or the lens-twist method.

Enter the aperture setting of the lens here to aid in the calculation of absolute exposure values to aid in day/night feathering of interval and exposure compensation.

Option | Description
------ | -------
[aperture] | Aperture value that the lens is set to or locked on (in the case of lens-twist)


## Destination

This option is only shown when an SD card is inserted in the VIEW.

Option | Description
------ | -------
Camera | Keep images on the camera's card.  For auto ramping, XMP files will need to be later saved and merged with the camera files (to be described in the post-processing section coming soon).
SD Card | Saves the time-lapse images in their own folder in the root of the SD card, along side the XMP files for Lightroom.  This simplifies post-processing and organization since the exposure corrections for deflickering will be automatically imported into Lightroom along with the images.

## START

If you have all the settings entered, select this option to start the time-lapse!  While it's running, you can select "Preview" to review the results in process, or select "RUNNING" for a cancellation confirmation.  This status screen is still in its most basic state and will be improved in a future release.





