# Motion Control

The VIEW is able to synchronize with most motion control systems for shoot-move-shoot functionality.  In addition it has full motion programming support for the Dynamic Perception NMX stepper controller (via Bluetooth or USB), with support for the eMotimo Spectrum (via AUX2 serial) and Syrp Genie Mini (via Bluetooth) to come soon.

## AUX Out Sync

To trigger a motion system to move after each shot, connect a 2.5mm TRS cable from AUX2 on the VIEW to the sync input on the motion system.  The VIEW will send a 200ms "closed" pulse after the completion of each shot.

## External Trigger

If the motion system does not support an external auxiliary sync (like the Syrp Genie), the VIEW can use the camera trigger from the motion system to trigger each frame.  In this mode, the interval is defined externally by the motion system.

To use an external trigger, set the Interval Mode to 'External AUX2' in the time-lapse setup menu.  Connect the motion system's camera port to the VIEW's AUX2 port.

## NMX Controller

In addition to the above methods, the NMX can be connected via USB or Bluetooth for full motion programming.  Motion programming must be done via the mobile app for the VIEW as it is not currently supported by the standalone interface.

### NMX Bluetooth Connection

To connect the NMX via Bluetooth, first enable Bluetooth on the VIEW in Settings->Wireless Setup->Enable Bluetooth.  The VIEW must be restarted after enabling Bluetooth (this will be fixed in the future so the restart is not necessary).  With Bluetooth enabled, the VIEW will automatically connect to the first available NMX controller.

### NMX USB Connection

To connect to the NMX via USB, a USB hub is needed for the additional USB port (one for the camera, one for the NMX).  Connect a small USB hub to the VIEW, then connect the camera and the NMX to the hub, then connect power to the NMX (in this order!).

Important: the NMX must first be connected via USB, then external power -- if the NMX is powered on before connecting USB, it won't be detected.
