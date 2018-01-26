# Mysensors hardware Package Lists for the Arduino v1.6.4+ Board Manager 

This repo contains the custom `package_*_index.json` files that can be used to add new
third party boards to the Arduino v1.6.4+ IDE.

To add MySensors to Boards Manager list, go to IDE preferences, and at the bottom of the dialog add the following URL into "Additional boards managers URLs:" field and hit OK:

https://raw.githubusercontent.com/mysensors/ArduinoBoards/master/package_mysensors.org_index.json

![Arduino preferences dialog](/screenshot/arduino-preferences-dialog.png?raw=true "Arduino preferences dialog")

For the Sensebender Gateway, you'll need to install the Arduino SAMD board as well. Otherwise, you'll get this error:
```
The current selected board needs the core 'arduino:arduino' that is not installed.
```

## List of 3rd Party Boards

https://github.com/arduino/Arduino/wiki/Unofficial-list-of-3rd-party-boards-support-urls
