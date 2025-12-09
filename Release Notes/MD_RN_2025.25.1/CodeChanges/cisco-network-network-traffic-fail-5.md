# Code Changes for cisco-network-network-traffic-fail-5 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'cisco-mma-kv-network-traffic-firewall', 'cisco-mma-kv-network-traffic-firewall-1') && !InList(toLower(result), 'allow','allow all') |