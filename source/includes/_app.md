# Remote App

The VIEW Intervalometer can be controlled and monitored via a web-based app for mobile devices.  Anything with a web browser can access it, but it's only optimized for mobile-sized screens.  There is no app publish in an app store at this point, rather, it is loaded directly from the VIEW itself.

There are two methods for connecting to the VIEW from a mobile device, a local WiFi method, and an internet method.

### Local Method Pros:

* No Internet required, works in remote locations
* Low-latency connections, great with streaming liveview during setup

### Local Method Cons:

* Only works within WiFi range of the VIEW
* Internet will not function on the mobile device while connected to the VIEW

### Web Method Pros:

* Access the VIEW from anywhere in the world!
* Mobile device can be connected to the internet as usual

### Web Method Cons:

* The VIEW needs to be within range of a WiFi access point for internet (you could use a mobile hotspot)
* Higher latency so you'll see some lag with liveview



## Local Wifi Method

![WiFi Setup Diagram](view-app-wifi.png)

To configure the local WiFi app interface, setup the following on the VIEW:

1. Enable WiFi (if it's not already): Settings -> Wireless Setup -> Enable Wifi
2. Enable Access Point Mode: Settings -> Wireless Setup -> Enable built-in AP (if this setting is missing it means it's already enabled)

Then, on the mobile device:

1. Connect to the TL+VIEW WiFi access point*
2. Open a web browser and go to 10.0.0.1

That's it -- the app will then load in the browser.  On an iPhone, you can save it to the homescreen for convenient use as a full-screen app.

The name of the built-in access point can be changed under Settings -> Wireless Setup -> Set built-in AP Name.

* Note: In v1.8 and newer, a password is required.  The default is "timelapse+" and it can be viewed/changed in Settings->Wireless Setup->Set built-in AP Password

## Remote Internet Method

![Web Setup Diagram](view-app-web.png)

To configure the remote web app interface, setup the following on the VIEW:

1. Enable WiFi (if it's not already): Settings -> Wireless Setup -> Enable Wifi
2. Connect to a nearby access point: Settings -> Wireless Setup -> Connect to Network
3. Enter the password for the network if necessary (make sure it's entered correctly with the correct case).  Use the context button on the lower right to switch between uppercase/lowercase/numbers/symbols.  Press the power button on the password screen for more instructions.
4. Once the VIEW connects (only the first time), a number will appear on the screen.  You'll need this for step 4 below.

Then, on the mobile device:

1. Open a web browser and go to app.view.tl
2. Login using your email address.  If you need to register, you'll be asked to create a subdomain (for access as yoursubdomain.view.tl) and a password
3. Once logged in, if this is your first time, press 'Add Device' (if you've done this before, you don't need to again)
4. Enter the numbers displayed on the VIEW screen

That's it -- the app will then load in the browser.  On an iPhone, you can save it to the homescreen for convenient use as a full-screen app.



