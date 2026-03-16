# Code Changes for unix-sendmail-email-send-success-1 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'unix-sm-kv-email-send')InList(type, 'unix-sm-kv-email-delay') && (StartsWith(toLower(result), 'sent')) |