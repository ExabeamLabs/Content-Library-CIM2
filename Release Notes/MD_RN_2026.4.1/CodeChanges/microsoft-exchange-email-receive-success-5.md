# Code Changes for microsoft-exchange-email-receive-success-5 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type,'microsoft-x-csv-email-deliver', 'microsoft-exchange-json-email-receive-incoming') && (!exists(result) || (exists(result) && result='Success')) && InList(toLower(action),'deliver','receive','redirect','send','haredirect','hareceive') |