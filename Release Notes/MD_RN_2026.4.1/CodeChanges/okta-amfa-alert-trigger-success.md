# Code Changes for okta-amfa-alert-trigger-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'okta-amfa-mix-app-login-success-securitycontext','okta-amfa-cef-alert-trigger-success-threatdetected', 'okta-amfa-cef-app-login-success-appadloginsuccess', 'okta-amfa-cef-app-login-success-coreuserauthloginsuccess', 'okta-amfa-cef-app-login-fail-coreuserauthloginfailed', 'okta-amfa-cef-app-login-fail-appadloginbadpassword') && (InList(operation, 'security.threat.detected','security.zone.request.blocked','user.account.report_suspicious_activity_by_enduser') || InList(operation, 'system.idp.lifecycle.read_client_secret')) |