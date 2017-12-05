# Motion Control

The VIEW is able to synchronize with most motion control systems for shoot-move-shoot functionality.  In addition it has full motion programming support for the Dynamic Perception NMX stepper controller (via Bluetooth or USB) and Syrp Genie Mini (via Bluetooth), with support for the eMotimo Spectrum (via AUX2 serial) and Syrp Genie Mini (via Bluetooth) to come soon.

## AUX Out Sync

To trigger a motion system to move after each shot, connect a 2.5mm TRS cable from AUX2 on the VIEW to the sync input on the motion system.  The VIEW will send a 200ms "closed" pulse after the completion of each shot.

## External Trigger

If the motion system does not support an external auxiliary sync (like the Syrp Genie), the VIEW can use the camera trigger from the motion system to trigger each frame.  In this mode, the interval is defined externally by the motion system.

To use an external trigger, set the Interval Mode to 'External AUX2' in the time-lapse setup menu.  Connect the motion system's camera port to the VIEW's AUX2 port.

## Dynamic Perception NMX

In addition to the above methods, the NMX controller can be connected via USB or Bluetooth for full motion programming.  Motion programming must be done via the mobile app for the VIEW as it is not currently supported by the standalone interface.

### NMX Bluetooth Connection

<i>Note: for this method, the latest v1.8 beta firmware should be installed on the VIEW.</i>  To connect the NMX via Bluetooth, first enable Bluetooth on the VIEW in Settings->Wireless Setup->Enable Bluetooth (if it only shows "Disable Bluetooth", then it's already enabled).  Make sure the NMX app is not connected to the NMX, as this will block the VIEW from connecting (turn BT off on the phone if needed).  With Bluetooth enabled, the VIEW will automatically connect to the first available NMX controller when it is powered on.  A small Bluetooth icon will appear in the top bar of the VIEW once connected.  It can then be setup via the VIEW wifi app as show in this video: https://vimeo.com/237150285

### NMX USB Connection

To connect to the NMX via USB, a USB hub is needed for the additional USB port (one for the camera, one for the NMX).  Connect a small USB hub to the VIEW, then connect the camera and the NMX to the hub, then connect power to the NMX (in this order!).  It's recommended to have BT disabled on both the VIEW and the phone in this case to avoid any issues.  A small Bluetooth icon will appear in the top bar of the VIEW once connected.  It can then be setup via the VIEW wifi app as show in this video: <https://vimeo.com/237150285>

USB has the advantage of being more reliable and not affected by cold temperatures.

Important: the NMX must first be connected via USB, then external power -- if the NMX is powered on before connecting USB, it won't be detected.

## Syrp Genie Mini

The VIEW can fully control the Syrp Genie Mini via Bluetooth, allowing for multi-keyframe motion programming.  The latest v1.8 beta firmware is required on the VIEW, and the Genie Mini should also have its firmware up to date.  Note that when controlling the Genie Mini via the VIEW it will not be possible to use the Syrp app at the same time, so it's best to disable BT on the phone to avoid interference.  

To connect the Genie Mini to the VIEW, first enable Bluetooth on the VIEW in Settings->Wireless Setup->Enable Bluetooth (if it only shows "Disable Bluetooth", then it's already enabled).  Then power on the Genie Mini and watch for a small Bluetooth icon to appear in the top bar in the VIEW's display.  At present, up to two Genie Minis can be connected at once (like for pan/tilt).  Each one can be then configured in the VIEW's wifi app, similar to the NMX setup show here: <https://vimeo.com/237150285>.  Also see <https://vimeo.com/235979676> for a quick setup without the app.

If preferred, the Genie Mini can also be programmed separately and then synchronized with the VIEW for shoot move shoot functionality.  This is the "External Trigger" method shown above.  Connect the camera port on the Genie Mini to the AUX2 port in the VIEW with a 2.5mm TRS cable (TRRS will not work) and then set the Interval Mode on the VIEW to 'External AUX2'.  In this configuration, the VIEW fires each frame when prompted by the Mini while handling ramping, and the Mini manages the motion and interval as defined in the Syrp app.