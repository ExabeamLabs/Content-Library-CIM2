# Code Changes for cisco-network-network-traffic-fail-4 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type,'cisco-netflow-str-network-traffic-success-ipaccesslog') AND InList(toLower(result), 'denied','blocked','dropped') |