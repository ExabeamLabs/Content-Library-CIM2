# Code Changes for servicenow-s-json-http-session-success-transcation (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_details', 'additional_info', 'alert_id', 'category', 'dest_user', 'event_name', 'group_name', 'item_name', 'operation', 'operator_name', 'priority', 'status_msg', 'sub_category', 'task_id'] |
| edit_regex_field | event_name |  | ['exa_regex=\&sys_display.incident.short_description=?({operation}({event_name}[^&]+?))\s*\&', 'exa_regex=\&sys_original.sc_task.short_description=?({operation}({event_name}[^&]+?))\s*\&'] |
| added_regex_field | operation |  | ['exa_regex=\&sys_display.incident.short_description=?({operation}({event_name}[^&]+?))\s*\&', 'exa_regex=\&sys_original.sc_task.short_description=?({operation}({event_name}[^&]+?))\s*\&'] |
| removed_attribute | DupFields |  | N/A |
| added_attribute | incident_creation_timeFormat |  | yyyy-MM-dd HH:mm:ss |