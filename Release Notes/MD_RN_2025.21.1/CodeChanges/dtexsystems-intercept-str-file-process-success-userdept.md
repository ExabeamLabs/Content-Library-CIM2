# Code Changes for dtexsystems-intercept-str-file-process-success-userdept (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'activity_details', 'bytes', 'domain', 'file_dir', 'host', 'host_domain', 'operation', 'operation_details', 'os_architecture', 'os_edition', 'os_type', 'os_version', 'process_dir', 'process_name', 'src_file_dir', 'src_file_ext', 'src_file_name', 'src_host', 'time', 'url', 'user'] |
| edit_regex_field | host |  | ['(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){11}(({host_domain}[^\\]+)\\)?({src_host}({host}[\w\-\.]+))?'] |
| edit_regex_field | host_domain |  | ['(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){11}(({host_domain}[^\\]+)\\)?({src_host}({host}[\w\-\.]+))?'] |
| edit_regex_field | operation |  | ['(?:[^,]*,){6}({access}({operation}[^,]+))?'] |
| added_regex_field | access |  | ['(?:[^,]*,){6}({access}({operation}[^,]+))?'] |
| added_regex_field | src_host |  | ['(?:([^",]*,)){10}(".+?"|[^,]*),(?:([^,]*,)){11}(({host_domain}[^\\]+)\\)?({src_host}({host}[\w\-\.]+))?'] |
| removed_attribute | DupFields |  | N/A |