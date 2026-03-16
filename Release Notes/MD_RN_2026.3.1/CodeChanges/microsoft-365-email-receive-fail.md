# Code Changes for microsoft-365-email-receive-fail (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type , 'microsoft-o365-json-email-send-receive-subject' ,'microsoft-o365-cef-email-send-receive-subject', 'microsoft-o365-sk4-email-receive-success-inbound') and (InList(toLower(result),'failed','filteredasspam', 'quarantined') or (exists(action) and InList(toLower(action), 'quarantine', 'delivery failed', 'dropped'))) |