# Code Changes for lumension-l-kv-peripheral-storage-insert-success-mediuminserted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bytes', 'dest_host', 'device_class', 'device_id', 'device_pid', 'device_vid', 'domain', 'file_ext', 'file_name', 'file_path', 'host', 'operation', 'operation_details', 'time', 'user', 'user_sid'] |
| edit_regex_field | host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d(:|-)\d\d(:|-)\d\dZ) (|({dest_host}({host}[\w\-.]+))) scomc.+?({operation}\S+) \['] |
| edit_regex_field | operation |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d(:|-)\d\d(:|-)\d\dZ) (|({dest_host}({host}[\w\-.]+))) scomc.+?({operation}\S+) \['] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d(:|-)\d\d(:|-)\d\dZ) (|({dest_host}({host}[\w\-.]+))) scomc.+?({operation}\S+) \['] |
| added_regex_field | dest_host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d(:|-)\d\d(:|-)\d\dZ) (|({dest_host}({host}[\w\-.]+))) scomc.+?({operation}\S+) \['] |
| removed_attribute | DupFields |  | N/A |