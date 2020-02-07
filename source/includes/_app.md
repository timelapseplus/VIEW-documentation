# Remote App

The VIEW Intervalometer can be controlled and monitored via an app for mobile devices.  There's also a web-app version so that anything with a web browser can access it, although it's only optimized for mobile-sized screens.  

TL+VIEW app for iOS: <a href='https://apps.apple.com/us/app/tl-view/id1412185976' target='_blank'>https://apps.apple.com/us/app/tl-view/id1412185976</a>
TL+VIEW app for Android: <a href='https://play.google.com/store/apps/details?id=com.timelapseplus.view' target='_blank'>https://play.google.com/store/apps/details?id=com.timelapseplus.view</a>

Regardless of whether you use the native app or the web interface, there are two methods for connecting to the VIEW from a mobile device: a local WiFi method, and an internet method.

### Local WiFi Pros:

* No Internet required, works in remote locations
* Low-latency connections, great with streaming liveview during setup

### Local WiFi Cons:

* Only works within WiFi range of the VIEW
* Internet will not function on the mobile device while connected to the VIEW's WiFi network

### Internet Method Pros:

* Access the VIEW from anywhere in the world!
* Mobile device can be connected to the internet as usual

### Internet Method Cons:

* The VIEW needs to be within range of a WiFi access point for internet (you could use a mobile hotspot)
* Higher latency so you'll see some lag with liveview



## Connecting via local Wifi

![WiFi Setup Diagram](view-app-wifi.png)

To configure the local WiFi app interface, setup the following on the VIEW:

1. Enable WiFi (if it's not already): Settings->Wireless Setup->Enable Wifi
2. Enable Access Point Mode: Settings->Wireless Setup->Enable built-in AP (if this setting is missing it means it's already enabled)

Then, on the mobile device:

1. Connect to the TL+VIEW WiFi access point*
2. Open the TL+VIEW app, or use a web browser and go to 10.0.0.1

The name of the built-in access point can be changed under Settings->Wireless Setup->Set built-in AP Name.

* Note: In v1.8 and newer, a password is required.  The default is "timelapse+" and it can be viewed/changed in Settings->Wireless Setup->Set built-in AP Password

## Connecting via the Internet

![Web Setup Diagram](view-app-web.png)

To access the VIEW over the internet, setup the following on the VIEW:

1. Enable WiFi (if it's not already): Settings->Wireless Setup->Enable Wifi
2. Connect to a nearby access point: Settings->Wireless Setup->Connect to Network
3. Enter the password for the network if necessary (make sure it's entered correctly with the correct case).  Use the context button on the lower right to switch between uppercase/lowercase/numbers/symbols.  Press the power button on the password screen for more instructions.
4. Once the VIEW connects (only the first time), a number will appear on the screen.  You'll need this for step 4 below.

Then, on the mobile device:

1. Open the TL+VIEW app or use a web browser and go to <a href='https://app.view.tl' target='_blank'>https://app.view.tl</a>
2. Login or register using your email address.
3. Once logged in, if this is your first time, press 'Add Device' (if you've done this before, you don't need to again)
4. Enter the numbers displayed on the top of the VIEW screen (or find them in Information->Registration & App) -- this links your device to your app account


## Using the app

The app has 4 sections: CAMERA, INTERVALOMETER, TIME-LAPSE CLIPS, and SETTINGS.  To switch between sections, press the menu icon on the upper left of the app, or swipe right from the left edge of the screen to open the menu.

### CAMERA

This section allows manual control of the camera for taking single images, changing settings, and using liveview.  This can function as a remote trigger for the camera.  

Beneath the image box at the top, there is a round LV button on the right -- press this to enable the liveview display.  In the center is a blue button which will capture a single image.  On the left is a 2 second timer -- the camera will capture an image after 2 seconds.

Further down, there are tabs to switch between different controls:
- Exposure - change the shutter, aperture and ISO on the camera
- Focus - move the focus position manually (if supported)
- Motion - move various motion axes (if supported and connected)

### INTERVALOMETER

In this section you can setup, start, and monitor a time-lapse on the VIEW.  Note that once a time-lapse is started from the app, the app does not need to remain connected; it runs independantly on the VIEW.

The parameters are the same as found on the VIEW itself -- see <http://docs.view.tl/#time-lapse-setup> for details on each parameter.

There are a few things the app has in addition to the VIEW:

- Keyframe Motion
- Delayed Start
- Scheduled Time-lapse

Additionally, the app also allows changing parameters of a time-lapse that is running, whether it was started via the app or on the VIEW.

### TIME-LAPSE CLIPS

In this section you can review previous time-lapses capture with the VIEW.  If you tap a time-lapse, it will open and can be played back (in low-res).  

When a time-lapse is open there is a red button on the right to delete the clip (this deletes the low-res preview on the VIEW -- nothing else), and a blue button for copying the settings used from this clip and opening them in the INTERVALOMETER section to create a new time-lapse based on them.

Additionally, if there was a problem with the clip, a copy of the log file can be sent to support to aid in diagnosis of the problem using the link found at the bottom of the screen when viewing a time-lapse clip.  You will then receive an email -- please reply to that email with a description of the problem.

### SETTINGS

The SETTINGS section is somewhat minimal yet, but the following is available:

- Pair a new VIEW device (opens a dialog to enter the pairing number on a new device for linking it to your account)
- Configure Motion - this is available when a compatible motion system is connected and includes settings related to the specific motion system
- Logout -- this logs out the current user, in case you need to log back in with a different email or are using a shared system
