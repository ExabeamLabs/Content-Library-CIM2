# Code Changes for sophos-ep-cef-peripheral-storage-insert-success-alertedonly (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'device_class', 'domain', 'first_name', 'full_name', 'host', 'last_name', 'operation', 'operation_details', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | host |  | ['"location":"({host}[\w\-.]+)'] |
| removed_attribute | DupFields |  | N/A |