When I touch this NFC tag, take me to this dashboard (or any URL)

```
description: "When I touch an NFC card, take me to this dashboard"
mode: single
trigger:
  - platform: tag
    tag_id: 12345-12354-12345-12345
condition: []
tap_action: 
 action: navigate
 navigation_path: /dashboard/page
```

