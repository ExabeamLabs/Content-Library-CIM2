# Code Changes for symantec-dlp-kv-email-send-incident (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_severity', 'alert_type', 'dest_email_address', 'dest_email_domain', 'dest_ip', 'dest_port', 'device_id', 'domain', 'email_address', 'email_attachment', 'email_domain', 'email_recipients', 'email_subject', 'file_ext', 'file_name', 'host', 'message_id', 'occured_time', 'protocol', 'src_host', 'src_ip', 'src_port', 'target', 'time', 'url', 'user', 'web_domain'] |
| edit_regex_field | file_ext |  | [',\sattachment_filename="(([^"]+\\)?({email_attachment}[^"]+\.({file_ext}[a-zA-Z]{2,})))\s*",', ',\sattachment_filename="(([^"]+\\)?({file_name}[^"]+\.({file_ext}[a-zA-Z]{2,})))\s*",', ',\sfile_name="+(?:N\/A|({email_attachment}[^",]+?\.({file_ext}[^"\s]+)))\s*[^"]*"*,', ',\sfile_name="+(?:N\/A|({file_name}[^",]+?\.({file_ext}[^"\s]+)))\s*[^"]*"*,'] |
| added_regex_field | email_attachment |  | [',\sattachment_filename="(([^"]+\\)?({email_attachment}[^"]+\.({file_ext}[a-zA-Z]{2,})))\s*",', ',\sfile_name="+(?:N\/A|({email_attachment}[^",]+?\.({file_ext}[^"\s]+)))\s*[^"]*"*,'] |
| added_regex_field | email_subject |  | ['[\s,]subject="+(?:N\/A|({email_subject}(?:[^",]|"")+?))\s*"*,'] |
| added_regex_field | message_id |  | ['[\s,]incident_id="+({message_id}\d+)'] |
| added_regex_field | src_host |  | [',\sendpoint_machine="+(?:N\/A|({src_host}[^",]+?))\s*"*,\s'] |
| removed_attribute | DupFields |  | N/A |
| edit_attribute | SOAR |  | ConfigTree([('IncidentType', 'dlp'), ('NameTemplate', 'Symantec DLP Alert ${alert_name} found'), ('ProjectName', 'SOC'), ('EntityFields', [ConfigTree([('EntityType', 'device'), ('Name', 'src_address'), ('Fields', ['src_ip->ip_address'])]), ConfigTree([('EntityType', 'user'), ('Name', 'windows_id'), ('Fields', ['user->windows_id'])])])]) |