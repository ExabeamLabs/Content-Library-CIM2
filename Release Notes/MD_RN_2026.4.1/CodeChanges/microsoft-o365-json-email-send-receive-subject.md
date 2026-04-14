# Code Changes for microsoft-o365-json-email-send-receive-subject (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['"RecipientAddress":"', '"SenderAddress":"', '"Subject":', 'Id":"', 'MessageTrace'] |
| edit_regex_field | log_source |  | ['dproc=({log_source}[^"\s]+)', 'exa_regex=dproc=({log_source}[^"\s]+)'] |
| edit_regex_field | message_id |  | ['"MessageId":"({message_id}[^"]+)"', '"MessageTraceId":"({message_id}[^"]+)"', '"id":"({message_id}[^"]+)"'] |
| edit_regex_field | time |  | ['"Date":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)', '"Received":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?)', '"StartDate":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)', '"StartDate":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)', '"receivedDateTime":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d)', 'exa_regex="receivedDateTime":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d)'] |