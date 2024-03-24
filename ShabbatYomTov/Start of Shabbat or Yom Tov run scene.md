This automation uses both the Shabbat and Yom Tov sensors in order to start the automation when either sensor becomes true. 

In other words, when it's either Shabbat OR Yom Tov this automation will trigger and run:

```
alias: Start of Shabbat or Yom Tov automation
description: >-
  Puts home into Shabbat / Yom Tov configuration mode when either sensor turns
  to true.
trigger:
  - platform: state
    entity_id:
      - sensor.hebcal_is_shabbat
    to: "True"
  - platform: state
    entity_id:
      - sensor.hebcal_is_yomtov
    to: "True"
condition: []
action:
  - service: scene.turn_on
    metadata: {}
    target:
      entity_id: scene.start_of_shabbat
mode: single

```

