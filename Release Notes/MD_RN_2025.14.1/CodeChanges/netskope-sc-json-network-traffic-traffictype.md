# Code Changes for netskope-sc-json-network-traffic-traffictype (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| edit_attribute | activity_type | ['http-session:success', 'network-traffic:success'] | ['http-session:success', 'network-traffic:fail', 'network-traffic:success'] |
| edit_attribute | legacy_activity_type | ['network-connection-successful', 'web-activity-allowed'] | ['network-connection-failed', 'network-connection-successful', 'web-activity-allowed'] |