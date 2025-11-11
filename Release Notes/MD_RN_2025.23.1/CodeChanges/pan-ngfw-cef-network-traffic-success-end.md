# Code Changes for pan-ngfw-cef-network-traffic-success-end (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | action |  | ['\sapp=({action}(incomplete|insufficient-data))\s+(\w+=|$)', '\|({action}[^\|]+)\|TRAFFIC'] |
| removed_attribute | DupFields |  | N/A |