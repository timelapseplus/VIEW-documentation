# Camera-Specific Notes

This section includes notes and issues specific to certain camera bodies.  Camera-specific issues will be corrected in firmware when possible and removed from this section once resolved.

## Notes for all cameras

* Manual mode
* A native ISO setting (not Auto)
* Save as RAW (not RAW+JPEG)
* Focus should be manual or back-button (if the shutter button activates focus it can cause issues)
* It's best to disable image stabilization

## Sony Alpha (USB)

Sony cameras can work well, but there are several things that the VIEW currently does not enforce but must be set in the camera for it to work.

There have been reports that not all USB cables work with Sony cameras, so if it fails to connect, try a different USB cable.

Setup the following on the camera:

1. USB Mode set to 'PC Remote'
2. RAW files (not JPEG or RAW+JPEG)
3. Manual mode, in a native ISO (not the ISO numbers with a line over them, nor auto ISO)
4. Focus set to manual (the back button still works for autofocus, but this prevents it from trying to focus on every shot)

On the VIEW in the time-lapse setup menu, the Destination must be set to SD card.  Insert an SD card into the VIEW for this option to appear.  This is required because a limitation in the Sony firmware prevents it from being able to save to the camera's card while it's connected via USB.

The Sony A7RII needs longer intervals due to the large file size if using USB.  14 seconds should be good -- shorter might be possible.  Other Sony cameras seem to do ok at 6-8 seconds for a minimum interval.  With the Wifi interface this is not an issue.

## Sony Alpha (Wifi)

The best interface for Sony is wifi since it doesn't have the limitations imposed on the USB interface.

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

## Panasonic

Make sure the USB mode on the camera is set to PTP

## Camera Support Overview

Camera Body | Auto Ramping | Focus Ramping | Liveview | Minimum Ramping Interval
------------|--------------|---------------|----------|----------------- 
Nikon DSLRs | Yes          | Yes, most     | Yes, most| 3-4s
Canon DSLRs | Yes          | Yes, most     | Yes, most| 3-4s
Sony A7, A6000, A7S | Yes   | No            | No       | 8-12s via USB, 4-5s via Wifi
Sony A7R    | Yes          | No            | No       | 14-18s via USB, 4-5s via Wifi
Sony A7RII  | Yes          | No            | Yes      | 14-18s via USB, 4-5s via Wifi
Sony A7II, A6300, A6500, A7SII | Yes   | No            | Yes       | 8-12s via USB, 4-5s via Wifi
Panasonic GH4, GH5 | Yes          | No     | No | 4-7s
