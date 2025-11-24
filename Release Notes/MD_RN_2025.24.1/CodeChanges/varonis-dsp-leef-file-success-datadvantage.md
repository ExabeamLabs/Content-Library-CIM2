# Code Changes for varonis-dsp-leef-file-success-datadvantage (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'additional_info', 'alert_name', 'category', 'domain', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'full_name', 'result', 'src_host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | access |  | ['Event_Type=({event_code}({access}.+?))\s+(\w+=|$)'] |
| edit_regex_field | alert_name |  | ['DatAdvantage\|[^\\]+?\|({additional_info}({alert_name}[^\\]+?))\|'] |
| added_regex_field | additional_info |  | ['DatAdvantage\|[^\\]+?\|({additional_info}({alert_name}[^\\]+?))\|'] |
| added_regex_field | event_code |  | ['Event_Type=({event_code}({access}.+?))\s+(\w+=|$)'] |
| removed_attribute | DupFields |  | N/A |