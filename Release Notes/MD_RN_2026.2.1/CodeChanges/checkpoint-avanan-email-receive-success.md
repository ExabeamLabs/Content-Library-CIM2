# Code Changes for checkpoint-avanan-email-receive-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type,'checkpoint-avanan-json-email-receive-securityevent','checkpoint-avanan-json-email-send-receive-phishing','checkpoint-avanan-json-email-receive-avanansecurityevent', 'checkpoint-avanan-json-email-receive-entitypayload', 'checkpoint-avanan-json-email-entitypayload') && InList(toLower(result), 'false') |