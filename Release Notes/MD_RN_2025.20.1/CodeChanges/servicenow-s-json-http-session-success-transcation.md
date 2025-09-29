# Code Changes for servicenow-s-json-http-session-success-transcation (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['activity_details', 'additional_info', 'alert_id', 'category', 'dest_user', 'event_name', 'group_name', 'operator_name', 'priority', 'status_msg', 'sub_category'] |
| removed_regex_field | state |  | [] |
| added_regex_field | status_msg |  | ['exa_json_path=$.url,exa_regex=sys_original.incident.state=({status_msg}.*?)\&incident.reopen_count'] |