# Code Changes for wazuh-ping-app-template-dl (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'agent_id', 'agent_name', 'app', 'decoder_name', 'description', 'email_address', 'event_name', 'host', 'log_location', 'log_path', 'result', 'rule_id', 'src_ip', 'src_port', 'time', 'user', 'wazuh_manager'] |
| edit_regex_field | description |  | ['"rule.description":"({event_name}({description}[^"]+))'] |
| added_regex_field | event_name |  | ['"rule.description":"({event_name}({description}[^"]+))'] |
| removed_attribute | DupFields |  | N/A |