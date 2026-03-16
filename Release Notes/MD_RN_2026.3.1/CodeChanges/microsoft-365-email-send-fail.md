# Code Changes for microsoft-365-email-send-fail (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type , 'microsoft-o365-json-email-send-receive-subject' , 'microsoft-o365-cef-email-send-receive-subject','microsoft-o365-cef-email-send-workload', 'microsoft-o365-cef-email-send-sendas','microsoft-o365-sk4-email-send-fail-outbound') and (InList(toLower(result), 'failed', 'filteredasspam', 'quarantined') or (exists(action) and InList(toLower(action), 'quarantine', 'delivery failed', 'dropped'))) |