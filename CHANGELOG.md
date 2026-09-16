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

## 0.4.5
- Highlight a requested fan mode immediately instead of waiting for the Modbus polling round trip.
- Reconcile the optimistic fan selection with the confirmed ESPHome entity state.
- Clear an unconfirmed selection after 12 seconds or immediately on a service error.

## 0.4.6
- Always highlight the selected fan command rather than the current physical fan output.
- Keep immediate optimistic feedback for Home Assistant fan selections.
- Continue treating Actual Fan Speed as an optional informational reading only.

## 0.5.0
- Move room temperature, humidity, active setpoint, user setpoint, cooling target, and heating target into the upper climate summary.
- Make Cooling target and Heating target selectable while sharing one large value and one pair of adjustment buttons.
- Add an optional 24-hour room-temperature sparkline using Home Assistant recorder history.
- Color the graph for heating, cooling, or off state.
- Remove the separate Current readings section.

## 0.5.1
- Open a styled numeric popup when the large target value is clicked.
- Submit typed values with Set or Enter and cancel with Cancel or Escape.
- Snap typed values to the configured temperature interval.
- Make plus and minus move to the next valid interval boundary, even if the current value is off-step.
- Respect the selected number entity's minimum and maximum.

## 0.5.2
- Correct the center target button dimensions so the full temperature value is clickable.
- Supersedes version 0.5.1.

## 0.5.3
- Keep the target-temperature popup open during Home Assistant state updates.
- Refresh the card with accumulated state changes after the popup closes.

## 0.6.0
- Replace the informational tiles with plain inline room, humidity, active-setpoint, and user-setpoint values.
- Keep only Cooling target and Heating target as rounded clickable tiles.
- Replace the temperature-only sparkline with a shared 24-hour temperature and humidity graph.
- Use separate graph colors and a compact legend.
- Remove the target-selection instructional text.

## 0.6.1
- Correct optional-value cleanup so an empty summary row cannot remove the main target control.
- Supersedes version 0.6.0.

## 0.7.0
- Move the shared temperature/humidity graph to the bottom of the card.
- Make room temperature the large read-only value in the upper section.
- Evenly distribute humidity, active setpoint, and user setpoint beneath room temperature.
- Remove the main-section plus and minus controls.
- Open the target popup directly when Cooling target or Heating target is clicked.
- Add interval-aware plus and minus controls inside the target popup.
