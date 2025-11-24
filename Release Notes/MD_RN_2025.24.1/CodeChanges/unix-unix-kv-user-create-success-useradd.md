# Code Changes for unix-unix-kv-user-create-success-useradd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_id', 'account_name', 'dest_user', 'host', 'process_id', 'process_name', 'src_host', 'time'] |
| edit_regex_field | account_name |  | ['new user: name\\*=({dest_user}({account_name}[^,]+)),'] |
| edit_regex_field | host |  | ['(\s|T)\d\d:\d\d:\d\d(\.?\S+)? ({src_host}({host}[\w.\-]+))\suseradd', '({time}\w+\s\d+\s\d\d:\d\d:\d\d)?\s*({src_host}({host}[\w.\-]+))\suseradd'] |
| edit_regex_field | time |  | ['({time}\w+\s\d+\s\d\d:\d\d:\d\d)?\s*({src_host}({host}[\w.\-]+))\suseradd', '\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\+\-][^\s]+)'] |
| added_regex_field | dest_user |  | ['new user: name\\*=({dest_user}({account_name}[^,]+)),'] |
| added_regex_field | src_host |  | ['(\s|T)\d\d:\d\d:\d\d(\.?\S+)? ({src_host}({host}[\w.\-]+))\suseradd', '({time}\w+\s\d+\s\d\d:\d\d:\d\d)?\s*({src_host}({host}[\w.\-]+))\suseradd'] |
| removed_attribute | DupFields |  | N/A |