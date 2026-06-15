# Code Changes for epic-siem-database-query-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'epic-siem-cef-database-query-success-verbosekbsqlqueryrun') and InList(operation, 'VERBOSE_KB_SQL_QUERY_RUN') |