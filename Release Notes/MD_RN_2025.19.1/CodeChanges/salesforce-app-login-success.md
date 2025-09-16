# Code Changes for salesforce-app-login-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'salesforce-sf-json-app-login-success-loginurl', 'salesforce-sf-json-app-activity-success-loginhistory') && exists(result) && InList(toLower(result),'success','login_no_error') |