# Code Changes for jamf-jamfpro-json-security-alerts-jamfprotect (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | TimeFormat |  | epoch_sec |
| changed | Conditions |  | ['"eventType":', '"facts":', '"human":', '"input":', '"match":', '"matchReason":', '"protectVersion":', '"provisioningUDID":'] |
| changed_parsed_fields | N/A |  | ['file_dir', 'file_name', 'file_path', 'process_dir', 'process_name', 'process_path', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | time |  | ['exa_json_path=$.input.match.event.timestamp,exa_regex=^({time}\d{10})'] |