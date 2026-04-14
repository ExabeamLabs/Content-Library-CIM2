# Code Changes for corelight-corelightids-json-alert-trigger-success-suricatacorelight (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_ip', 'src_host', 'src_ip', 'tactic', 'tactic_key', 'technique', 'technique_key'] |
| added_regex_field | tactic |  | ['exa_json_path=$.[\'alert.metadata\'][6],exa_regex=mitre_tactic_name:({tactic}[^"]+)'] |
| added_regex_field | tactic_key |  | ['exa_json_path=$.[\'alert.metadata\'][5],exa_regex=mitre_tactic_id:({tactic_key}[^"]+)'] |
| added_regex_field | technique |  | ['exa_json_path=$.[\'alert.metadata\'][8],exa_regex=mitre_technique_name:({technique}[^"]+)'] |
| added_regex_field | technique_key |  | ['exa_json_path=$.[\'alert.metadata\'][7],exa_regex=mitre_technique_id:({technique_key}[^"]+)'] |