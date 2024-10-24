# Changelog

## 0.1.8

- Switch to grott beta
- Feature parity with stable addon

## 0.1.7

- migrate away from goss to pytest
- unit test of the container
- Support for expire of measurements

## 0.1.6

- Add support for versionned grott
- Use grot 2.8.3

## 0.1.5

- Update template
- Update documentation

## 0.1.4

- Switch to use grott-ha-plugin

## 0.1.3

- Fixed CURL version

## 0.8

Added an option to improve compatibility with [grott homeassistant integration](https://github.com/muppet3000/homeassistant-grott).

To activate this mode, you can disable the HA integration in the configuration and enable the grott_mqtt flag. This will configure the MQTT for pushing information through the grott MQTT exporter.

## 0.7

- Add new options for configuration
  - Verbose mode
  - MQTT retain
  - data path, now you can edit your configuration in /config/grott/grott.ini
  - Allow custom MQTT broker

## 0.6

- Updated the branch used by grott

## 0.5

- Change to use pip3 with the newest addon image.

## 0.3

- Add translations
- Moved the ginvtypemap to the top configuration

## 0.2

- Based on grott v2.7.7
- use the current grott_ha.py plugins
- Auto configuration for the MQTT part

## 0.1

- Initial version
- Based on grott v2.7.6
