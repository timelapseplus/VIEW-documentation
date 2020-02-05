# Motion Control

The VIEW is able to synchronize with most motion control systems for shoot-move-shoot functionality.  In addition it has full motion programming support for the Dynamic Perception NMX stepper controller (via Bluetooth or USB) and Syrp Genie Mini (via Bluetooth), with support for the eMotimo Spectrum (via AUX2 serial) and Kessler Second Shooter (likely) planned for the near future.

## AUX Out Sync

To trigger a motion system to move after each shot, connect a 2.5mm TRS cable from AUX2 on the VIEW to the sync input on the motion system.  The VIEW will send a 200ms "closed" pulse (with default settings) after the completion of each shot.  No special setup is required on the VIEW.  The motion system needs to support an external intervalometer input, and usually needs to be in a special mode (e.g., "slave" mode for the NMX, "external intervalometer" for eMotimo TB3).

The pulse parameters can be adjusted in Settings->

## External Trigger

This is the most versatile option and should work with any system that has a camera trigger for shoot-move-shoot.  This is the only option for systems that don't support an external auxiliary sync (like the Syrp Genie). In this mode, the interval is defined externally by the motion system, and the VIEW works inline between the motion system and the camera to handle the exposure.

To use an external trigger, set the Interval Mode to 'External AUX2' in the time-lapse setup menu.  Connect the motion system's camera port to the VIEW's AUX2 port with a 2.5mm TRS cable (TRRS won't work). The camera is connected to the VIEW's USB port as usual.  Once started, the VIEW will then wait for the signal from the motion system to trigger each frame.

With this configuration, the VIEW handles the exposure and ramping, and the motion and interval is defined by the motion system.  Since the VIEW is not controlling the interval, a variable interval is not possible.

## Dynamic Perception NMX

In addition to the above methods, the NMX controller can be connected via USB or Bluetooth for full motion programming.  Motion programming must be done via the mobile app for the VIEW as it is not currently supported by the standalone interface.

### NMX Bluetooth Connection

<i>Note: for this method, the latest v1.8 beta firmware should be installed on the VIEW.</i>  To connect the NMX via Bluetooth, first enable Bluetooth on the VIEW in Settings->Wireless Setup->Enable Bluetooth (if it only shows "Disable Bluetooth", then it's already enabled).  Make sure the NMX app is not connected to the NMX, as this will block the VIEW from connecting (turn BT off on the phone if needed).  With Bluetooth enabled, the VIEW will automatically connect to the first available NMX controller when it is powered on.  A small Bluetooth icon will appear in the top bar of the VIEW once connected.  It can then be setup via the VIEW wifi app as show in this video: <a href='https://vimeo.com/237150285' target='_blank'>https://vimeo.com/237150285</a>

### NMX USB Connection

To connect to the NMX via USB, a USB hub is needed for the additional USB port (one for the camera, one for the NMX).  Connect a small USB hub to the VIEW, then connect the camera and the NMX to the hub, then connect power to the NMX (in this order!).  It's recommended to have BT disabled on both the VIEW and the phone in this case to avoid any issues.  A small Bluetooth icon will appear in the top bar of the VIEW once connected.  It can then be setup via the VIEW wifi app as show in this video: <a href='https://vimeo.com/237150285' target='_blank'>https://vimeo.com/237150285</a>

USB has the advantage of being more reliable and not affected by cold temperatures.

Important: the NMX must first be connected via USB, then external power -- if the NMX is powered on before connecting USB, it won't be detected.


## eMotimo Spectrum (ST4)

The VIEW can fully control the eMotimo ST4 with a USB to serial data cable (a direct AUX2 data connection is also in development).  VIEW Firmware v1.8 or newer is required.  To set this up, use a USB hub to connect both the camera and the ST4 to the VIEW's single USB port, and connect the data cable to the ST4's I/O port.  Make sure to set the I/O port on the ST4 to the eMotimo API.

Setup video: <a href='https://vimeo.com/338113886' target='_blank'>https://vimeo.com/338113886</a>

## Syrp Genie Mini

<aside class="warning">IMPORTANT: Syrp removed support for the VIEW in the new firmware installed by the new Genie II app.  To fix this, connect to the Genie Mini with the older GenieApp (with the VIEW bluetooth turned off so it doesn't interfere) and it will install the old firmware (it may prompt for it).  After the old firmware is installed on the Genie Mini, close the GenieApp and turn the phone's bluetooth off, then re-enable Bluetooth on the VIEW and it should be fully working.</aside>

The VIEW can fully control the Syrp Genie Mini via Bluetooth, allowing for multi-keyframe motion programming.  The latest v1.8 beta firmware is required on the VIEW, and the Genie Mini should also have its firmware up to date.  Note that when controlling the Genie Mini via the VIEW it will not be possible to use the Syrp app at the same time, so it's best to disable BT on the phone to avoid interference.  

To connect the Genie Mini to the VIEW, first enable Bluetooth on the VIEW in Settings->Wireless Setup->Enable Bluetooth (if it only shows "Disable Bluetooth", then it's already enabled).  Then power on the Genie Mini and watch for a small Bluetooth icon to appear in the top bar in the VIEW's display.  At present, up to two Genie Minis can be connected at once (like for pan/tilt).  Each one can be then configured in the VIEW's wifi app, similar to the NMX setup show here: <a href='https://vimeo.com/237150285' target='_blank'>https://vimeo.com/237150285</a>.  Also see <a href='https://vimeo.com/235979676' target='_blank'>https://vimeo.com/235979676</a> for a quick setup without the app.

If preferred, the Genie Mini can also be programmed separately and then synchronized with the VIEW for shoot move shoot functionality.  This is the "External Trigger" method shown above.  Connect the camera port on the Genie Mini to the AUX2 port in the VIEW with a 2.5mm TRS cable (TRRS will not work) and then set the Interval Mode on the VIEW to 'External AUX2'.  In this configuration, the VIEW fires each frame when prompted by the Mini while handling ramping, and the Mini manages the motion and interval as defined in the Syrp app.  For a video on how this is setup, see <a href='https://www.facebook.com/syrp.co.nz/videos/1183817961718350/' target='_blank'>https://www.facebook.com/syrp.co.nz/videos/1183817961718350/</a>