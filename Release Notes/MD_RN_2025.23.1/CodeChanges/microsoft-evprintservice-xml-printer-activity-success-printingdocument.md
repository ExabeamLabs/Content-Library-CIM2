# Code Changes for microsoft-evprintservice-xml-printer-activity-success-printingdocument (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'activity_1', 'activity_2', 'additional_info', 'bytes', 'channel', 'dest_host', 'dest_ip', 'dest_port', 'error_code', 'event_code', 'file_name', 'host', 'num_pages', 'object', 'printer_name', 'result', 'run_level', 'src_host', 'src_ip', 'src_port', 'time', 'user', 'user_sid'] |
| edit_regex_field | object |  | ['<Message>[^,]+,\s+({file_name}({object}.+?))\s+owned by', '<Param2>({file_name}({object}[^<]+))<'] |
| added_regex_field | file_name |  | ['<Message>[^,]+,\s+({file_name}({object}.+?))\s+owned by', '<Param2>({file_name}({object}[^<]+))<'] |
| removed_attribute | DupFields |  | N/A |