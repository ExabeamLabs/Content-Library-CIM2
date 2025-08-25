# Code Changes for symantec-dlp-kv-email-send-incident (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | activity_type |  | ['alert-trigger:success', 'email-send:fail', 'email-send:success'] |
| edit_attribute | legacy_activity_type |  | ['dlp-alert', 'dlp-email-alert-out', 'dlp-email-alert-out-failed'] |