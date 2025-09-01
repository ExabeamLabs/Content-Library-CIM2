# Code Changes for servicenow-s-json-http-session-success-transcation (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_details', 'additional_info', 'alert_id', 'category', 'dest_user', 'event_name', 'group_name', 'operator_name', 'priority', 'state', 'sub_category'] |
| added_regex_field | activity_details |  | ['exa_json_path=$.url,exa_regex=\&incident.work_notes=({activity_details}.*?)\&sys_display.incident.comments'] |
| added_regex_field | additional_info |  | ['exa_json_path=$.url,exa_regex=sys_original.incident.description=({additional_info}.*?)\&incident.closed_by'] |
| added_regex_field | alert_id |  | ['exa_json_path=$.url,exa_regex=sys_original.incident.number\=({alert_id}.*?)\&sysparm_record_target'] |
| added_regex_field | category |  | ['exa_json_path=$.url,exa_regex=sys_original.incident.category=({category}.*?)\&incident.opened_at'] |
| added_regex_field | dest_user |  | ['exa_json_path=$.url,exa_regex=sys_display.incident.assigned_to=({dest_user}.*?)\&sys_original.incident.work_notes'] |
| added_regex_field | event_name |  | ['exa_json_path=$.url,exa_regex=sys_display.incident.short_description=({event_name}.*?)\&sysparm_record_list'] |
| added_regex_field | group_name |  | ['exa_json_path=$.url,exa_regex=sys_display.incident.assignment_group=({group_name}.*?)\&sysparm_ck'] |
| added_regex_field | operator_name |  | ['exa_json_path=$.url,exa_regex=sys_original.incident.sys_updated_by=({operator_name}.*?)\&sys_display.original.incident.caller_id'] |
| added_regex_field | priority |  | ['exa_json_path=$.url,exa_regex=sys_original.incident.priority=({priority}.*?)\&sys_original.incident.comments'] |
| added_regex_field | state |  | ['exa_json_path=$.url,exa_regex=sys_original.incident.state=({state}.*?)\&incident.reopen_count'] |
| added_regex_field | sub_category |  | ['exa_json_path=$.url,exa_regex=sys_original.incident.subcategory=({sub_category}.*?)\&incident.caused_by'] |
| added_attribute | DupFields |  | ['time->incident_creation_time', 'event_name->operation'] |