# Code Changes for splunk-digitalguardian-usb-insert (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'device_class', 'device_id', 'domain', 'event_code', 'host', 'operation_details', 'time', 'user'] |
| edit_regex_field | host |  | ['Computer_Name="([^\/\\"]+[\/\\]+)?({dest_host}({host}[\w\-.]+))"'] |
| added_regex_field | dest_host |  | ['Computer_Name="([^\/\\"]+[\/\\]+)?({dest_host}({host}[\w\-.]+))"'] |
| removed_attribute | DupFields |  | N/A |