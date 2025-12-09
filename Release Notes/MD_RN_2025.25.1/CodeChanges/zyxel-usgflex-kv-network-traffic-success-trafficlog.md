# Code Changes for zyxel-usgflex-kv-network-traffic-success-trafficlog (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | bytes_in |  | ['\srcvd=({bytes_in}\d+)', 'rcvd=({bytes_in}\d+)'] |
| edit_regex_field | bytes_out |  | ['\ssent=({bytes_out}\d+)', 'sent=({bytes_out}\d+)'] |