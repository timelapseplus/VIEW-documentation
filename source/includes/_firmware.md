# Firmware Update

The VIEW Intervalometer can be updated on its own -- no computer is necessary, just a wifi access point for Internet access.

The firmware is loaded directly from github releases, so you can also browse the available firmware here: <a href='https://github.com/timelapseplus/VIEW/releases/' target='_blank'>github.com/timelapseplus/VIEW/releases/</a>

The current firmware version is displayed on the top line of the screen.

### Step 1: Connect the VIEW to the internet

The VIEW must first be connected to the Internet.  Follow these to connect to a WiFi access point for Internet access:

1. Enable WiFi (if it's not already): Settings -> Wireless Setup -> Enable Wifi
2. Connect to a nearby access point: Settings -> Wireless Setup -> Connect to AP
3. Enter the password for the network if necessary (make sure it's entered correctly with the correct case).  Use the context button on the lower right to switch between uppercase/lowercase/numbers/symbols.  Press the power button on the password screen for more instructions.

You can ignore any prompts to enter a code -- just press the cancel button.

### Step 2: Update firmware

Next, navigate to Settings -> Software Version.  If it's successfully connected to the Internet, it will delay a few seconds while it retreives the latest firmware information.  If it's not connected to the Internet, it will only show the previously installed versions (this is so you can always roll back, even when there's no Internet available).  If it just loads the installed versions, return to step 1 above and verify the network password is correct or try a different access point.

Once the Software Version menu has loaded, you can select the firmware version to install.  Press the power button to read the release notes for the selected version.  Press the knob or the enter button to install the selected version.  Updating to the most recent version is always recommended.

The installation will take between 5 and 30 minutes, depending on the connection quality.  Upon success, the system wil reload, displaying the boot splash screen.  If it fails, it will return to the Software Versions menu (better feedback in the UI will be added for this in the future).

Firmware updates will either fail or succeed -- it won't get stuck in a corrupted state.  That said, it's possible for it to hang when downloading if there's a network interruption (working on fixing this).  If after 15 minutes or so the VIEW still says it's downloading the firmware, it may need a force-restart.  Hold the power button for fifteen seconds to power down, then 2 seconds to boot it back up.  It will load the old firmware version, and then you can try again to update.  A future update will provide better error handling & reporting and progress reporting (like a progress bar for the download).

