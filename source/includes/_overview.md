# Overview and Operation

## Power and Buttons

![Front Overview](images/view-overview-front.png)

### Power On

To power on the VIEW, press and hold the Power button `(#1)` for 2 seconds.  In a few seconds the button will illuminate red, indicating that it's booting.  The VIEW logo will appear on the screen shortly thereafter. 

### Power Off

To power off the VIEW, press and hold the Power button `(#1)` for 2 seconds.  A confirmation prompt will appear on the screen.  Turn the knob to select "Yes" and 
press the knob or the Enter button `(#5)` to power off.

If the VIEW is not responsive, it can be forced off by pressing holding the Power button `(#1)` for 15 seconds.  It can then be booted normally by pressing the Power button again for 2 seconds.

### Operation

The user interface for the VIEW is a menu based system designed to be simple to operate outdoors and with gloves.  For that reason, there's no touchscreen, but rather simple buttons and a knob for scrolling through options.  Use the knob to scroll up and down through the menus.  To select open or select the highlighted menu item, press the knob or the Enter button `(#5)`.  To go back or cancel, press the Cancel button `(#4)`.  Some screens use the Context `(#6)` button for additional options indicated on the screen.

<aside class="success">Every menu item has an accompanying help screen -- press the Power button (#1) to activated for the current selection.  Power the Power button (#1) or the Cancel button (#4) to exit the help screen.</aside>

### Gesture Sensor

The Gesture Sensor `(#2)` while a time-lapse is running and the screen goes blank.  Wave your hand across the front to activate, then wave to the right to preview the current/last time-lapse, or to the left to cancel.  While the preview is playing, wave to the right to skip ahead 10 seconds.

## Ports and Connections

![Front Overview](images/view-overview-side.png)

### Charging

To charge the VIEW, connect a Micro-B USB cable from a USB power supply (USB charger, battery pack or computer) to the charging port `(#12)` on the VIEW.  When connected the Charge Indicator `(#11)` will illuminate red, blinking while charging, and steady when full.  This light can be disabled in Settings->Charge Indicator.  Note that the battery indicator in the VIEW will prematurely show a low battery, and if charging a completely dead battery, it can take some time before progress becomes visible.

### Auxiliary Ports

The VIEW includes two 2.5mm TRS auxiliary ports `(#9, #10)` for motion sync, shutter cable triggering and external integrations.  Currently only AUX2 is used by the firmware.  It will send a pulse to trigger motion systems to move after each shot during a time-lapse (no setup necessary for this), or it can be used as an external trigger for the interval when the time-lapse interval is set to "External".

### SD Card

The SD card slot `(#8)` provides a convenient way to get data from the VIEW.  The VIEW can also save the RAW time-lapse images to the SD card -- this is the most convenient way for post processing, since each time-lapse is named sequentially in its own folder along with the XMP files for automatic deflickering in Lightroom.

The VIEW supports all current SD card types and capacities, but internally it uses a Class 10 controller, so the newest UHS II cards will not offer a speed improvement over a Class 10 card.  Cards can be formatted with the camera or on a computer as FAT/EXFAT (MSDOS).

### USB Host

The VIEW includes a full-size USB host port `(#13)` for connecting the camera.  This port also supports USB hubs for connecting multiple devices (right now it can also communicate with the DP NMX via USB, and multiple camera support is planned for the future).

## Hooking up the camera

### Hotshoe Mount

The VIEW can be conveniently connected to the top of the camera by sliding it on the camera's hotshoe.  This also provides PC-sync feedback for bulb ramping without requiring an additional cable, however, the current exposure ramping mode does not use this, so you can mount the VIEW anywhere without affecting the performance.

### USB Connection

Connect the appropriate USB cable for your camera from the Host Port `(#13)` to your camera's USB port.  It's best to have the camera powered on before connecting, as there seems to be an occasional timing issue causing the camera to not properly connect if powered on while connected.  If the camera doesn't seem to connect, unplug the USB and reconnect.  Sony cameras can be quite flaky -- if you're having trouble, try removing the battery from the camera, powering it back on, and then plugging in the USB to the VIEW again.

Some cameras need to be set to "PC Connect" or "PTP Mode" in order for USB to function properly.  Also, some Canon cameras with WiFi (like the 6D) require WiFi to be disabled for USB control to work.

Only the USB cable is needed for full ramping support.  No other connections are necessary.









