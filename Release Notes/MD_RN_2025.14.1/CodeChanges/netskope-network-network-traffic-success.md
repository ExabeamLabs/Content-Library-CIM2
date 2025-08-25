# Code Changes for netskope-network-network-traffic-success (Event Builder)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| edit_conditions | expression | InList(type, 'netskope-sc-json-network-traffic-traffictype') && !(InList(toLower(protocol), 'http') || InList(dest_port,'443','80')) | InList(type, 'netskope-sc-json-network-traffic-traffictype', 'netskope-sc-json-network-traffic-traffictype-1') && !(InList(toLower(protocol), 'http') || InList(dest_port,'443','80')) && !InList(toLower(action), 'redirect', 'block') |