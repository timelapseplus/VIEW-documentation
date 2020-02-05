# Camera-Specific Notes

This section includes notes and issues specific to certain camera bodies.  Camera-specific issues will be corrected in firmware when possible and removed from this section once resolved.

## Notes for all cameras

* Manual mode
* A native ISO setting (not Auto)
* Save as RAW (not RAW+JPEG)
* Disable any long exposure noise reduction
* Focus should be manual or back-button (if the shutter button activates focus it can cause issues)
* It's best to disable image stabilization

## Sony Alpha (USB)

There are two groups of Sony cameras, the 1st and second generation ones and the new 3rd generation cameras (A7rIII, A9, A7III).  The 3rd generation cameras allow the RAW images to be kept on the camera allowing much faster performance via USB.

There have been reports that not all micro-USB cables work with Sony cameras, so if it fails to connect, try a different USB cable.  The new USB-C cables are a much more secure option on the cameras that support it.

Some Sony cameras allow charging while in use via the USB port.  If this is enabled, the VIEW's battery will drain rather quickly, so external power to the VIEW is recommended.  The VIEW cannot supply enough power to the camera to charge the battery during operation, but it will greatly extend the battery life.  So if you have a full battery in the camera and have a USB power source connected to the VIEW (like a cell phone charging pack), the whole setup should last at least 12 hours before the camera's battery slowly drains (varies depending on camera and interval).

### 1st and 2nd generation Sony Alphas

This includes the A6000, A6300, A6500, A7, A7r, A7s, A7rII, A7sII, A7II.

1st and 2nd generation Sony cameras can work well, but there are several things that the VIEW currently does not enforce but must be set in the camera for it to work.

Setup the following on the camera:

1. USB Mode set to 'PC Remote'
2. RAW files (not JPEG or RAW+JPEG)
3. Manual mode, in a native ISO (not the ISO numbers with a line over them, nor auto ISO)
4. Focus set to manual (the back button still works for autofocus, but this prevents it from trying to focus on every shot)
5. Make sure long exposure noise reduction is disabled

On the VIEW in the time-lapse setup menu, the Destination must be set to SD card.  Insert an SD card into the VIEW for this option to appear.  This is required because a limitation in the Sony firmware prevents it from being able to save to the camera's card while it's connected via USB.

The Sony A7RII needs longer intervals due to the large file size if using USB.  8 seconds should be good -- shorter might be possible.  Other Sony cameras seem to do ok at 4-5 seconds for a minimum interval.

### 3rd and 4th generation Sony Alphas

This includes the A7rIV (4th gen), A7rIII, A9 and A7III.  On these cameras, USB is the recommend connection method over wifi.

It is possible to save the RAW images to the camera to improve interval times.  These cameras now also support focus ramping with the VIEW as well.

Setup the following on the camera (3rd gen):

1. RAW + smallest JPEG possible
2. USB Mode set to 'PC Remote'
3. In PC Remote Settings, set Still Img Save Dest to 'PC+Camera', and set RAW+J PC Save Img to 'JPEG'
4. Manual mode, in a native ISO (not the ISO numbers with a line over them, nor auto ISO)
5. Focus set to manual (the back button still works for autofocus, but this prevents it from trying to focus on every shot)
6. Make sure long exposure noise reduction is disabled

Video for 3rd gen setup: <a href='https://vimeo.com/297232264' target='_blank'>https://vimeo.com/297232264</a>
Video for 4th gen setup: <a href='https://vimeo.com/386651214' target='_blank'>https://vimeo.com/386651214</a>

Focus ramping with Sony: <a href='https://vimeo.com/387080128' target='_blank'>https://vimeo.com/387080128</a>


## Sony Alpha (Wifi)

The Wifi interface allows the 1st and 2nd generation cameras to save the the camera's memory card, but in general is not as reliable as USB, which is now recommended since the new camera driver (in VIEW firmware v1.8).

To connect the camera via wifi:

1. On the camera, open the "Smart Remote Control" app (must be updated to the latest version to work!).
2. The camera will display the wifi information.  Press the "delete" button on the camera to display the password.
3. Connect the VIEW's wifi (Settings->Wireless Setup->Connect to Network) to the camera's, using the password shown on the camera screen.
4. The VIEW should show that the camera is connected within a few seconds, and the camera will enable liveview again.
5. IMPORTANT: press the menu button on the camera and make sure it's set to RAW+JPEG (small).  The setting here does not follow what the camera was previously set to, and RAW only is not an option, but RAW+JPEG (small) works.

When using the wifi interface, the time-lapse Destination setting must be set to "Camera".  Afterward, you can get the XMPs via the Time-lapse Clips menu.

At present, a limitation with Sony wifi is that since the wifi interface on the VIEW is used for the camera, it's not possible to use the remote app.  It might be possible in the future firmware release to have two wifi interfaces to work around this.


## Nikon

Many Nikon cameras have the option of whether liveview displays the simulated exposure or not.  If you are using the exposure menu or liveview via the app, you'll want to make sure the liveview display shows the exposure.  On the D800, this is toggled by a button on the lower-left.  On the D5100 and possible other older/lower-end models, it is not possible to simulate exposure with liveview.  In this case, a test photo can be used via the smartphone app.

Note: some VIEW devices would not connect to the Nikon D800/D800E until firmware version v1.7.5.  Updating to v1.7.5 or newer will fix this.

## Panasonic

Make sure the USB mode on the camera is set to PC Tether (for the GH3 & GH4 set it to "Remote Control (PTP)"), in manual mode, RAW, and single-shot burst mode.  For the GH5, GH5S, and G9, firmware v1.8-beta23 or newer is required for the VIEW.

Setup video: <a href='https://vimeo.com/349567517' target='_blank'>https://vimeo.com/349567517</a>

## Fuji X

Note: Fuji support requires v1.8-beta13 or newer firmware on the VIEW.  Make sure the USB mode on the camera is set to PC Auto.  ISO should be manually set to 200 or higher (160 or higher for the X-T3).

Some Fuji cameras allow charging while in use via the USB port.  In this case, the VIEW's battery will drain rather quickly, so external power to the VIEW is recommended.  When testing with a fully charged VIEW and full battery in an X-T2, I was able to get 1200 frames over 4 hours before the VIEW ran out of power (the camera still had battery since it was being charged by the VIEW).  The VIEW cannot supply enough power to the camera to charge the battery during operation, but it will greatly extend the battery life.  So if you have a full battery in the camera and have a USB power source connected to the VIEW (like a cell phone charging pack), the whole setup should last at least 12 hours before the camera's battery slowly drains.

## Olympus OM-D

Note: Olympus support requires v1.8-44 or newer firmware on the VIEW.  It has been tested with the E-M1, E-M1 II, and E-M5 II.  Make sure the USB mode on the camera is set to Camera+PC icon.  ISO should be manually set to 200 or higher, with long exposure noise reduction disabled.

Setup video: <a href='https://vimeo.com/351745255' target='_blank'>https://vimeo.com/351745255</a>



## Camera Support Overview

Camera Body | Auto Ramping | Focus Ramping | Liveview | Minimum Ramping Interval
------------|--------------|---------------|----------|----------------- 
Nikon DSLRs | Yes              | Yes, most | Yes, most| 3s
Nikon Z6, Z7 | Yes              | Yes      | Yes      | 3s
Canon EOS DSLRs | Yes              | Yes, most | Yes, most| 3s
Canon EOS M50 | Yes              | Yes | Yes | 3s
Canon EOS R, RP | Yes              | Yes | Yes | 4s
Sony A7, A6000, A7S | Yes      | No        | No (wifi yes)      | 4-5s via USB, 4-5s via Wifi
Sony A7R    | Yes              | No        | No (wifi yes)      | 7-8s via USB, 4-5s via Wifi
Sony A7RII  | Yes              | No        | Yes       | 7-8s via USB, 4-5s via Wifi
Sony A7II, A6300, A6500, A7SII | Yes | No  | Yes       | 4-5s via USB, 4-5s via Wifi
Sony A7III, A9 | Yes | Yes  | Yes       | 3s via USB, 4-5s via Wifi
Sony A7rIII | Yes | Yes  | Yes       | 4-5s via USB, 5-6s via Wifi
Sony A7rIV | Yes | Yes  | Yes       | 5-6s via USB, 5-6s via Wifi
Panasonic GH3, GH4 | Yes          | No     | No | 4-7s
Panasonic GH5, GH5S, G9 | Yes | No     | Yes | 3s
Fuji X-T1 | Yes | No | Yes | 5-8s
Fuji X-T2, X-H2, X-T3 | Yes | Yes | Yes | 3s
Fuji GFX | Yes | Yes | Yes | 4-5s
Fuji X-Pro2 | Yes | Yes | Yes | 3-4s
Olympus OM-D | Yes | Yes | Yes | 3s

