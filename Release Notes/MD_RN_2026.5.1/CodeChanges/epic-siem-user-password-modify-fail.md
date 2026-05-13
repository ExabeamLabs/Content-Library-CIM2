# Code Changes for epic-siem-user-password-modify-fail (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'epic-siem-leef-app-activity-securitysiem', 'epic-siem-cef-password-modify-fail-wpsecuserpasswordchangefail', 'epic-siem-cef-password-modify-fail-efailedpasswordchange') and InList(operation, 'E_FAILEDPASSWORDCHANGE','WPSEC_USER_PASSWORD_CHANGE_FAIL') |