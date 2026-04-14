# Code Changes for microsoft-o365-cef-email-send-receive-subject (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | activity_type |  | ['app-activity:success', 'email-receive:fail', 'email-receive:success', 'email-send:fail', 'email-send:success'] |
| edit_attribute | legacy_activity_type |  | ['app-activity', 'dlp-email-alert-in', 'dlp-email-alert-in-failed', 'dlp-email-alert-out', 'dlp-email-alert-out-failed'] |