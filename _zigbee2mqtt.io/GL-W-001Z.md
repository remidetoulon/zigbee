---
model: GL-W-001Z
vendor: Gledopto
title: Zigbee ON/OFF Wall Switch
category:
supports: on/off
image: /assets/images/devices/GL-W-001Z.jpg
zigbeemodel: 
compatible: [z2m]
mlink: 
link: 
link2: 
link3: 
---
 
{% raw %}
```yaml
switch:
  - platform: "mqtt"
    state_topic: "zigbee2mqtt/[FRIENDLY_NAME]"
    availability_topic: "zigbee2mqtt/bridge/state"
    payload_off: "OFF"
    payload_on: "ON"
    value_template: "{{ value_json.state }}"
    command_topic: "zigbee2mqtt/[FRIENDLY_NAME]/set"

sensor:
  - platform: "mqtt"
    state_topic: "zigbee2mqtt/[FRIENDLY_NAME]"
    availability_topic: "zigbee2mqtt/bridge/state"
    unit_of_measurement: "-"
    value_template: "{{ value_json.linkquality }}"
```
{% endraw %}


