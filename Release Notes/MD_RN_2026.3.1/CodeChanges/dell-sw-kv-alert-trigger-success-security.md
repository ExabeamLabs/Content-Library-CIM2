# Code Changes for dell-sw-kv-alert-trigger-success-security (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | activity_type |  | ['alert-trigger:success', 'network-traffic:fail', 'vpn-authentication:success', 'vpn-login:success', 'vpn-session:success'] |
| edit_attribute | legacy_activity_type |  | ['authentication-successful', 'network-alert', 'network-connection-failed', 'security-alert', 'vpn-connection', 'vpn-login'] |