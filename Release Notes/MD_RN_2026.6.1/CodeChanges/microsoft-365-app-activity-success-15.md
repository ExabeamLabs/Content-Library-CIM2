# Code Changes for microsoft-365-app-activity-success-15 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type , 'microsoft-o365-json-email-send-receive-subject', 'microsoft-o365-json-email-send-receive-subject-1') and !exists(direction) and InList(toLower(result), 'pending' ,'gettingstatus') |