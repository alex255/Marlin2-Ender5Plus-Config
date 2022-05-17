# Ender-5 Plus Configurations for Marlin Firmware for marlin 2.0.9.3

### Benefits

- set max hotend temp to 300 because the base hotend can handle this without problem.
- enable and config PIDTEMPBED
- increase max extrude lenght for longer bowden and filament change
- modify Z offset to correct value
- slow down the leveling and home Z speed ( the default is too fast for the machine )
- enable Z_MIN_PROBE_REPEATABILITY_TEST
- enable FILAMENT_RUNOUT_SCRIPT
- always enable auto leveling after home
- enable PREHEAT_BEFORE_LEVELING
- enable HOTEND_IDLE_TIMEOUT
- modify unload/load lenght to the real bowden lenght
- modify ADVANCED_PAUSE_FEATURE settings, and now work perfectly with and without screen (octoprint) 
- enable more M114 report options for octoprint

## Important

NOTE: The Ender-5 LCD stock firmware is only compatible with Creality firmware. The LCD standard UI will not function. This is expected.

## Marlin DGUS UI Instructions

The Ender-5 stock LCD can optionally use a [customized Marlin DGUS interface](https://github.com/coldtobi/Marlin_DGUS_Resources). With the stock LCD firmware Marlin can only be controlled from a host over USB.

- Format an SD card using the FAT32 filesystem with 4K cluster size.
- Copy the `DWIN_SET` folder to the SD card.
- Power off the printer and disassemble the front panel to get access to the LCD board.
- Insert the SD card into the slot on the back of the LCD (not the main SD slot).
- Power on the printer. The screen will turn blue and display several messages, finishing with "SD Card Process... END!".
- Remove the microSD card and power cycle the printer.
- Once it looks good reassemble the front panel. You may need to physically rotate the LCD by 180˚ for proper UI orientation.

## Restoring Factory Firmware

The original firmware can be restored by downloading the [Ender 5 Plus firmware](https://www.creality.com/download) from Creality. You can follow the same LCD flashing procedure using the Creality-provided `DWIN_SET` folder.

## Marlin DGUS UI Limitations

- The Information button (i) doesn't function.
- The Tools menu does not do anything at this time.
- If you press the Tools menu icon, enter another menu, then press "back" you will end up stuck at the Boot Screen. Touch anywhere on the screen to get back to the Status Screen.
