# Code Changes for salesforce-sf-cef-file-upload-success-cloud-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'app', 'email_address', 'file_ext', 'file_id', 'file_name', 'file_type', 'full_name', 'operation', 'src_file_ext', 'src_file_name', 'time', 'user'] |
| removed_regex_field | file_path |  | [] |
| edit_regex_field | operation |  | ['CEF:([^\|]*\|){5}({operation}(resource-uploaded|resource-deleted))'] |
| added_regex_field | file_id |  | ['filePath=({file_id}[^=]+?)\s+\w+='] |
| edit_attribute | activity_type |  | ['file-delete:success', 'file-upload:success'] |
| edit_attribute | legacy_activity_type |  | ['file-delete', 'file-upload'] |