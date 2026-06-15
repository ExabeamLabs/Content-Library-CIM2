# Code Changes for onelogin-o-app-activity-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'onelogin-o-kv-app-login-3005','onelogin-o-cef-app-login-assumingactinguserid','onelogin-o-json-app-login-success-applogin') && !InList(activity_id, '5', '6', '8', '14', '77', '78', '153', '154', '211') |