# Post Processing

For ramping, the VIEW uses XMP files to provide exposure correction data for Lightroom to eliminate flicker.  As such, for flicker-free results, the post-processing workflow needs to incorporate these files.

If the images were saved to the VIEW's SD card (Destination = 'SD card'), then the delicker data will already be there when imported into Lightroom.  Just be careful not to change the exposure slider.  All other sliders are ok in the develop mode.

If the images were saved to the camera (Destination = 'Camera'), then the XMPs need to be merged into the same folder as the RAW images.

To retrieve XMPs for clips that were saved to the camera, go to Time-lapse Clips, select the clip, then press the menu (lower right) button and select "Write XMPs to SD card".  This step is necessary even if an SD card was present in the VIEW while recording to the camera.

See the flow chart below for a rough overview of the process.

## Flowchart Overview

![Flowchart](images/post-flowchart.png)
