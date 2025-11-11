# Code Changes for microsoft-evsecurity-kv-endpoint-unlock-success-4801-5 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'event_code', 'event_name', 'host', 'login_id', 'time', 'user'] |
| edit_regex_field | host |  | ['(?i)(((audit|success)( |_)(success|audit))|information)(<\d+>|\s+)({dest_host}({host}[\w\-.]+))', 'Computer(\w+)?[\"\s]*(:|=)\s*\"?({dest_host}({host}[\w\-.]+?))(\"|\s)', '\d+-\d+-\d+T\d+:\d+:\d+([\+\-]\d+:\d+|Z)\s+({dest_host}({host}[\w\-.]+))\s'] |
| added_regex_field | dest_host |  | ['(?i)(((audit|success)( |_)(success|audit))|information)(<\d+>|\s+)({dest_host}({host}[\w\-.]+))', 'Computer(\w+)?[\"\s]*(:|=)\s*\"?({dest_host}({host}[\w\-.]+?))(\"|\s)', '\d+-\d+-\d+T\d+:\d+:\d+([\+\-]\d+:\d+|Z)\s+({dest_host}({host}[\w\-.]+))\s'] |
| removed_attribute | DupFields |  | N/A |