# Code Changes for microsoft-exchange-json-email-receive-incoming (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | activity_type |  | ['app-notification:success', 'email-receive:fail', 'email-receive:success'] |
| edit_attribute | legacy_activity_type |  | ['app-activity', 'dlp-email-alert-in', 'dlp-email-alert-in-failed'] |