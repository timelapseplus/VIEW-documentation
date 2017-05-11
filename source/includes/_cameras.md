# Camera-Specific Notes

This section includes notes and issues specific to certain camera bodies.  Camera-specific issues will be corrected in firmware when possible and removed from this section once resolved.

## Notes for all cameras

* Manual mode
* A native ISO setting (not Auto)
* Save as RAW (not RAW+JPEG)
* Focus should be manual or back-button (if the shutter button activates focus it can cause issues)
* It's best to disable image stabilization

## Sony Alpha

Sony cameras can work well, but there are several things that the VIEW currently does not enforce but must be set in the camera for it to work.

There have been reports that not all USB cables work with Sony cameras, so if it fails to connect, try a different USB cable.

Setup the following on the camera:

1. USB Mode set to 'PC Remote'
2. RAW files (not JPEG or RAW+JPEG)
3. Manual mode, in a native ISO (not the ISO numbers with a line over them, nor auto ISO)
4. Focus set to manual (the back button still works for autofocus, but this prevents it from trying to focus on every shot)

On the VIEW in the time-lapse setup menu, the Destination must be set to SD card.  Insert an SD card into the VIEW for this option to appear.  This is required because a limitation in the Sony firmware prevents it from being able to save to the camera's card while it's connected via USB.

The Sony A7RII needs longer intervals due to the large file size.  12 seconds should be good -- shorter might be possible.  Other Sony cameras seem to do ok at 6-8 seconds for a minimum interval.

## Nikon

Many (all?) Nikon cameras have the option of whether liveview displays the simulated exposure or not.  If you are using the exposure menu or liveview via the app, you'll want to make sure the liveview display shows the exposure.  On the D800, this is toggled by a button on the lower-left.

## Panasonic

Make sure the USB mode on the camera is set to PTP

## Camera Support Overview

Camera Body | Auto Ramping | Focus Ramping | Liveview | Minimum Ramping Interval
------------|--------------|---------------|----------|----------------- 
Nikon DSLRs | Yes          | Yes, most     | Yes, most| 5-6s
Canon DSLRs | Yes          | Yes, most     | Yes, most| 5-6s
Sony A7, A6000, A7S | Yes   | No            | No       | 8-10s
Sony A7R    | Yes          | No            | No       | 12-14s
Sony A7RII  | Yes          | No            | Yes      | 12-14s
Sony A7II, A6300, A6500, A7SII | Yes   | No            | Yes       | 8-10s
Panasonic GH4, GH5 | Yes          | No     | No | 6-8s

Note: firmware v1.7 (not yet released) will reduce the minimum ramping for Canon and Nikon to 3-4 seconds, and Sony to 4-5 seconds (via wifi).