# Code Changes for cisco-network-network-traffic-success-2 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type,'cisco-netflow-str-network-traffic-success-ipaccesslog','cisco-netflow-kv-network-traffic-success-nfc-id') AND (!exists(result) OR !InList(toLower(result), 'denied')) |