# Code Changes for symantec-esc-json-email-send-success-emailinfo (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_id', 'bytes', 'dest_email_address', 'dest_email_domain', 'direction', 'email_address', 'email_attachment', 'email_domain', 'email_recipients', 'email_subject', 'file_ext', 'file_name', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | email_attachment |  | ['\[\{"fileNameOrURL":"({file_name}({email_attachment}[^\.]+\.({file_ext}[^"]+)))', 'exa_json_path=$.emailInfo.filesAndLinks[0].fileNameOrURL,exa_regex=^({file_name}({email_attachment}[^\.]+\.({file_ext}[^"]+)))$'] |
| edit_regex_field | file_ext |  | ['\[\{"fileNameOrURL":"({file_name}({email_attachment}[^\.]+\.({file_ext}[^"]+)))', 'exa_json_path=$.emailInfo.filesAndLinks[0].fileNameOrURL,exa_regex=^({file_name}({email_attachment}[^\.]+\.({file_ext}[^"]+)))$'] |
| added_regex_field | file_name |  | ['\[\{"fileNameOrURL":"({file_name}({email_attachment}[^\.]+\.({file_ext}[^"]+)))', 'exa_json_path=$.emailInfo.filesAndLinks[0].fileNameOrURL,exa_regex=^({file_name}({email_attachment}[^\.]+\.({file_ext}[^"]+)))$'] |
| removed_attribute | DupFields |  | N/A |