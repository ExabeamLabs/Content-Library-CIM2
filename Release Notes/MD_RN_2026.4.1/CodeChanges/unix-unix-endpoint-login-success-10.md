# Code Changes for unix-unix-endpoint-login-success-10 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'unix-unix-mix-user-switch-success-susession','unix-unix-mix-user-switch-success-sshdsession','unix-unix-str-user-switch-success-pam_unix','unix-unix-json-user-switch-success-session') && exists(user_id) && ((exists(user) && exists(dest_user) && user=dest_user) || ((!exists(user) || !exists(dest_user)) && (user_id=dest_user_id || (dest_user='root' && user_id='0') || (dest_user!='root' && user_id!='0')))) |