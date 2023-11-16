# zha-quirks
ZHA quirks - for devices that do not behave properly and need some love

# Usage

1. Create a custom quirk dir in HA, e.g., /config/custom_zha_quirks
2. In configuration.yaml, point to this directory:
```
zha:
  custom_quirks_path: /config/custom_zha_quirks/
```
3. Download and put the chosen quirk file in the directory above.
4. Restart Home Assistant

# In case of errors or to support a new function

1. Enable debug log level
```
logger:
  default: info
  logs:
    homeassistant.components.zha: debug
    zigpy: debug
    zhaquirks: debug
```
2. Restart Home Assistant
3. Repeat actions that create errors or enable/disable functions on the device
4. Wait for another minimum 5 minutes
5. Download Home Assistant logs - attach them as a file in new issue

# Supported devices

## ts0601_temperature.py
```
        MODELS_INFO: [
            ("_TZE200_bq5c8xfe", "TS0601"),
            ("_TZE200_locansqn", "TS0601"),
        ],     
```

> quirk forked from [jacekk015](https://github.com/jacekk015/zha_quirks/blob/main/ts0601_temperature.py)