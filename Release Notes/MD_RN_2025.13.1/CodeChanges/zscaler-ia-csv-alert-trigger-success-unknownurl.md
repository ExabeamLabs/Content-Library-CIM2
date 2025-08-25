# Code Changes for zscaler-ia-csv-alert-trigger-success-unknownurl (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'app', 'bytes_in', 'bytes_out', 'company', 'department', 'email_address', 'email_domain', 'file_dir', 'file_name', 'time'] |
| removed_regex_field | file_path |  | [] |
| added_regex_field | file_dir |  | ['"({file_dir}[^"]+)",("[^"]*",){6}"Unknown URL"'] |