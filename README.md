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

## Command to update / build the MySensors board package

The scripts are written in Python and require Python 3.4 or later.
```
pip3 install --user click gitpython
```

Run the check-updates command to have the tool scan the source package repositories and compare their platform.txt versions to the versions published in the board index. The tool will alert you of packages which are not up to date in the index. Run the tool as follows (use python, not python3 on Windows in all the subsequent commands):
```
python bpt.py check-updates
```

To update the MySensors packages run the following commands:
```
python bpt.py update-index "MySensors AVR Boards"
python bpt.py update-index "MySensors SAMD Boards"
python bpt.py update-index "MySensors nRF5 Boards"
```