# Code Changes for salesforce-sf-sk4-file-read-success-resourceviewed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'email_address', 'file_ext', 'file_name', 'file_type', 'operation', 'report', 'result_code', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | file_ext |  | ['\Wfname=(|({report}({file_name}.+?(\.({file_ext}\w+))?)))(\s+\w+=|\s*$)'] |
| edit_regex_field | file_name |  | ['\Wfname=(|({report}({file_name}.+?(\.({file_ext}\w+))?)))(\s+\w+=|\s*$)'] |
| added_regex_field | report |  | ['\Wfname=(|({report}({file_name}.+?(\.({file_ext}\w+))?)))(\s+\w+=|\s*$)'] |
| removed_attribute | DupFields |  | N/A |