# Code Changes for epic-siem-user-password-modify-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'epic-siem-leef-app-activity-securitysiem', 'epic-siem-cef-password-modify-success-eadminpasswordchange', 'epic-siem-cef-password-modify-success-eselfpasswordchange', 'epic-siem-cef-password-modify-success-wpsecuserpasswordchange') and InList(operation, 'E_ADMINPASSWORDCHANGE', 'E_SELFPASSWORDCHANGE', 'WPSEC_USER_PASSWORD_CHANGE') |