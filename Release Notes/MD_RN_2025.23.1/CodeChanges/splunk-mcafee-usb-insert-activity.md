# Code Changes for splunk-mcafee-usb-insert-activity (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'bytes', 'dest_host', 'dest_ip', 'dest_port', 'device_class', 'device_id', 'domain', 'file_name', 'operation', 'operation_details', 'time', 'user'] |
| edit_regex_field | operation |  | ['RulesToDisplay="({operation_details}({operation}[^"]+))'] |
| added_regex_field | operation_details |  | ['RulesToDisplay="({operation_details}({operation}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |