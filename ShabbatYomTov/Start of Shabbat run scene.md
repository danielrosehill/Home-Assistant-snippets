Basic YAML for starting Shabbat automations and scenes by using the excellent [Jewish Sabbaths Holidays HA integration](https://github.com/rt400/Jewish-Sabbaths-Holidays).

This YAML uses the binary "is it Shabbat?" sensor to run a scene for setting lighting for the start of Shabbat.

Swap with your own parameters, obviously!

```
alias: Start of Shabbat automation
description: "Puts home into Shabbat configuration mode "
trigger:
  - platform: state
    entity_id:
      - sensor.hebcal_is_shabbat
    to: "True"
condition: []
action:
  - service: scene.turn_on
    metadata: {}
    target:
      entity_id: scene.start_of_shabbat
mode: single

```

