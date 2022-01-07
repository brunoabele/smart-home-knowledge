# smart-home-knowledge

## Pair hue lamps to Zigbee4mqtt
Problem: My Zigbee setup (using a CC... usb stick) did not recognize new hue bulb, when I wanted to get rid of the now outdated old hue bridge model. 
I tried to just delete the bulb from the hue bridge, but this was not sufficient. There are several tips around to use the Hue dimming remote or some IKEA remotes, but I do not have them. Finally I found this solution which worked well, if you still have a hue bridge: https://www.homeandsmart.de/philips-hue-leuchten-zuruecksetzen

Steps: 
1. activate join in zigbee2mqtt (allow some longer time as the next steps are not so fast)
2. Screw the bulb into a socket where you can switch the light on and off easily and fast, and set power to "on", so the bulb emits light
3. Make sure your hue brigde is online and is found in the hue app
4. remove the hue bulb from the hue bridge by deleting the lamp in the hue app, if still visible in the app
5. Now use the hue app to search for the lamp again, but: Enter the 6-letter serial number in the search entry frust. This number is printed on the bulp near the screw socket.
6. After a few seconds, the bulb will go out for a short moment to signal a successful reset. Immediately, turn the power "off", otherwise the lamp will join the hue bridge network again.
7. Deactivate the hue bridge, e.g. by removing the power
8. Now switch to bulb power to "on" again, lamp should now connect to your zigbee4mqtt network

