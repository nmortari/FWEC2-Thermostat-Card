# Changelog

## 0.1.0
- Initial HACS-compatible release.
- Mode, fan, setpoint, live reading, output, economy, dehumidification, and alarm display.
- Home Assistant control ownership safety switch.

## 0.2.0
- Nimbus-inspired visual redesign with a dark floating surface.
- Heating and cooling ambient glow states.
- More compact typography, controls, readings, and status rows.

## 0.2.2
- Show heating and cooling target temperatures simultaneously.
- Retain the mode-aware large target control and all live FWEC2 readings.

## 0.3.0
- Add a native Home Assistant visual card editor.
- Add domain-filtered selectors for every FWEC2 entity.
- Add visual fields for the card title and temperature adjustment step.
- Keep YAML configuration fully supported.

## 0.3.1
- Let Sections dashboards calculate the card's natural height.
- Increase the masonry size estimate to prevent following cards from overlapping.

## 0.3.2
- Make the HA control button reliable when clicking its icon, label, or background.
- Use Home Assistant's generic toggle service for the configured control entity.

## 0.3.3
- Bind the HA control button directly after every card render.
- Explicitly call switch.turn_on and switch.turn_off.
- Display Home Assistant service-call errors inside the card.

## 0.3.4
- Correct the diagnostic control-button build.
- Supersedes version 0.3.3.

## 0.4.0
- Expand the HA control button to the right third of the card header.
- Highlight enabled HA control in yellow.
- Preserve active mode highlighting while HA control is disabled.
- Show actual fan-speed highlighting while HA control is disabled.

## 0.4.1
- Remove a stale responsive CSS fragment that affected desktop layout.
- Preserve the new one-third HA-control button and live status highlighting.

## 0.4.2
- Hide unassigned reading and status entities from the card.
- Hide an entire readings or status section when none of its entities are assigned.
- Make room temperature and humidity optional in the visual editor.

## 0.4.3
- Simplify the header to show only the card title and HA-control button.
- Remove the mode icon and mode/fan subtitle from the header.
- Remove the disabled-control informational notice.
- Give longer card titles more available width.

## 0.4.4
- Increase the card-title font from 15px to 17px.
- Bind every mode, fan, temperature, and HA-control button directly after rendering.
- Retain visible service-call error reporting for all controls.
