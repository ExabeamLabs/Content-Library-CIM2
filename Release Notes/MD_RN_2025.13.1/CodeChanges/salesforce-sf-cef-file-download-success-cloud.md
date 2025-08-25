# Code Changes for salesforce-sf-cef-file-download-success-cloud (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'app', 'domain', 'email_address', 'email_domain', 'file_ext', 'file_id', 'file_name', 'file_type', 'first_name', 'full_name', 'last_name', 'operation', 'time', 'user'] |
| removed_regex_field | file_path |  | [] |
| added_regex_field | file_id |  | ['filePath=({file_id}[^=]+?)\s+\w+='] |