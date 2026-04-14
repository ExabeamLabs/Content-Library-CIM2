# Code Changes for oracle-db-json-database-query-success-returncode (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", 'yyyy-MM-dd HH:mm:ss.SSSSSS'] |
| edit_attribute | activity_type |  | ['database-query:fail', 'database-query:success'] |