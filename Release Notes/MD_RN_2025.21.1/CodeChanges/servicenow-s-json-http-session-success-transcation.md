# Code Changes for servicenow-s-json-http-session-success-transcation (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_details', 'additional_info', 'alert_id', 'category', 'dest_user', 'event_name', 'group_name', 'item_name', 'operator_name', 'priority', 'status_msg', 'sub_category', 'task_id'] |
| edit_regex_field | activity_details |  | ['exa_json_path=$.url,exa_regex=\&incident.work_notes=({activity_details}.*?)\&sys_display.incident.comments', 'exa_json_path=$.url,exa_regex=sc_task.comments=({activity_details}.*?)\&sys_original.sc_task.state='] |
| edit_regex_field | additional_info |  | ['exa_json_path=$.url,exa_regex=sys_original.incident.description=({additional_info}.*?)\&incident.closed_by', 'exa_json_path=$.url,exa_regex=sys_original.sc_task.description=({additional_info}.*?)\&sc_task.request_item'] |
| edit_regex_field | dest_user |  | ['exa_json_path=$.url,exa_regex=sys_display.incident.assigned_to=({dest_user}.*?)\&sys_original.incident.work_notes', 'exa_json_path=$.url,exa_regex=sys_display.sc_task.assigned_to=({dest_user}.*?)\&sysparm_pop_onLoad'] |
| edit_regex_field | event_name |  | ['exa_json_path=$.url,exa_regex=sys_display.incident.short_description=({event_name}.*?)\&sysparm_record_list', 'exa_json_path=$.url,exa_regex=sys_original.sc_task.short_description=({event_name}.*?)\&onLoad_sys_updated_on='] |
| edit_regex_field | group_name |  | ['exa_json_path=$.url,exa_regex=sys_display.original.incident.assignment_group=({group_name}.*?)\&activity_filter', 'exa_json_path=$.url,exa_regex=sys_display.original.sc_task.assignment_group=({group_name}.*?)\&sys_display.original.sc_task.request.requested_for='] |
| added_regex_field | item_name |  | ['exa_json_path=$.url,exa_regex=sys_display.sc_task.request_item=({item_name}.*?)\&sys_original.sc_task.request_item.u_requested_for.user_name='] |
| added_regex_field | task_id |  | ['exa_json_path=$.url,exa_regex=sys_original.sc_task.number=({task_id}.*?)\&sc_task.request.requested_for='] |