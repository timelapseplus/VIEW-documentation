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

Setup the following on the camera:

1) USB Mode set to 'PC Remote'
2) RAW files (not JPEG or RAW+JPEG)
3) Manual mode, in a native ISO (not the ISO numbers with a line over them, nor auto ISO)
4) Focus set to manual (the back button still works for autofocus, but this prevents it from trying to focus on every shot)

On the VIEW in the time-lapse setup menu, the Destination must be set to SD card.  Insert an SD card into the VIEW for this option to appear.  This is required because a limitation in the Sony firmware prevents it from being able to save to the camera's card while it's connected via USB.

Also, on the VIEW, don't use the exposure menu (Sony doesn't support liveview), instead setup the exposure using the camera.

The Sony A7RII needs longer intervals due to the large file size.  12 seconds should be good -- shorter might be possible.  Other Sony cameras seem to do ok at 6-8 seconds for a minimum interval.
