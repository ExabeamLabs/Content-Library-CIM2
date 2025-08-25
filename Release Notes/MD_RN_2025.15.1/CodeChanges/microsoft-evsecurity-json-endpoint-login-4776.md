# Code Changes for microsoft-evsecurity-json-endpoint-login-4776 (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | event_id | ['"eventRecordID":"({event_id}\d+)"'] | ['"eventRecordID":"({event_id}\d+)"', '"record_id":"({event_id}\d+)"'] |
| edit_regex_field | host | ['"(Hostname|MachineName)":"({host}[^"]*)', '"Computer"+:"+({host}[\w\-.]+)"', '"Computer"+:"+({host}[\w\-.]+)"'] | ['"(Hostname|MachineName)":"({host}[^"]*)', '"Computer"+:"+({host}[\w\-.]+)"', '"Computer(_name)?"+:"+({host}[\w\-.]+)"'] |
| edit_regex_field | result | ['"severityValue":"({result}[^"]+?)\s*"'] | ['"severityValue":"({result}[^"]+?)\s*"', 'keywords":\["({result}[^"]+)"'] |
| edit_regex_field | result_code | ['"Status":"({result_code}[^"]*)'] | ['"Status":"({result_code}[^"]*)"'] |
| edit_regex_field | time | ['"EventTime":({time}\d+)', '"EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)', '"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,3})?Z)"', '"systemTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)'] | ['"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,3})?Z)', '"EventTime":({time}\d+)', '"EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)', '"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,3})?Z)"', '"systemTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+)'] |