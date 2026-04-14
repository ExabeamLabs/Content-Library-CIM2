# Code Changes for unix-auditd-user-switch-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'unix-auditd-kv-user-switch-success-sessionopen') && ((exists(user) && exists(dest_user) && user!=dest_user) || ((!exists(user) || !exists(dest_user)) && user_id!=account_id)) && !InList(toLower(login_type_text), 'cron') |