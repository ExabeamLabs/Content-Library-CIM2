# Code Changes for unix-unix-kv-endpoint-login-fail-ruser (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_id |  | ['\s({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2})\S+\s+(::ffff:)?({host}[^\s]+)\s+({process_name}[^\s]+)\s+({process_id}\d+)\s', '\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |
| edit_regex_field | process_name |  | ['\s({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2})\S+\s+(::ffff:)?({host}[^\s]+)\s+({process_name}[^\s]+)\s+({process_id}\d+)\s', '\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*'] |