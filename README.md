# FWEC2 Thermostat Card

A responsive Home Assistant dashboard card for a Daikin FWEC2 thermostat exposed as separate ESPHome entities.

## Install with HACS

1. Open HACS, choose **Dashboard**, then **Custom repositories**.
2. Add `https://github.com/nmortari/FWEC2-Thermostat-Card` as category **Dashboard**.
3. Install **FWEC2 Thermostat Card** and refresh Home Assistant.
4. Add a Manual card using the example below and replace every entity ID with yours.

```yaml
type: custom:fwec2-thermostat-card
title: Living Room
entities:
  ha_control: switch.home_assistant_control
  mode: select.thermostat_state
  fan_command: select.fan_command
  heating_setpoint: number.heating_setpoint_command
  cooling_setpoint: number.cooling_setpoint_command
  room_temperature: sensor.room_temperature
  humidity: sensor.humidity
  active_setpoint: sensor.active_setpoint
  user_setpoint: sensor.current_user_setpoint
  actual_fan: sensor.actual_fan_speed
  economy: binary_sensor.economy_active
  dehumidification: binary_sensor.dehumidification_active
  cooling_output: binary_sensor.cooling_output_vc
  heating_output: binary_sensor.heating_output_vh
  alarm: binary_sensor.alarm
```

If your select labels differ, map them exactly:

```yaml
mode_options:
  off: "Off"
  heating: "Heating"
  cooling: "Cooling"
fan_options:
  automatic: "Automatic"
  low: "Low"
  medium: "Medium"
  high: "High"
temperature_step: 0.5
```

Readings remain live while HA control is disabled. Commands are intentionally locked until HA control is enabled.

## Visual editor

Version 0.3.0 and newer supports Home Assistant's graphical card editor. Add or edit the card from the dashboard UI, expand **FWEC2 entities**, and select each entity from the filtered dropdowns. YAML remains available for advanced configuration.
