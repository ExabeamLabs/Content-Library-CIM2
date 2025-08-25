# Code Changes for trendmicro-network-network-traffic-fail (Event Builder)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| edit_conditions | expression | InList(type, 'trendmicro-ds-cef-network-traffic-trendmicrodstenant','trendmicro-ds-kv-network-traffic-success-detectonly') && containsAny(toLower(operation), 'deny', 'reset') && !exists(alert_severity) && !exists(alert_name) | InList(type, 'trendmicro-ds-cef-network-traffic-trendmicrodstenant','trendmicro-ds-kv-network-traffic-success-detectonly') && containsAny(toLower(operation), 'deny', 'reset') && (!exists(alert_severity) || !exists(alert_name)) |