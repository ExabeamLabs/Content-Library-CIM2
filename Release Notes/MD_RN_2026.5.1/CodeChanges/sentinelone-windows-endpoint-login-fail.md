# Code Changes for sentinelone-windows-endpoint-login-fail (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'sentinelone-singularityp-json-endpoint-login-success-winlogonattempt', 'sentinelone-singularityp-json-endpoint-login-success-logins') && InList(toLower(os),'windows') && exists(failure_reason) && InList(toLower(result),'false') |