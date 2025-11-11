# Code Changes for cyberark-pam-leef-appactivityfile-vault (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'action', 'app', 'domain', 'email_address', 'email_domain', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'file_type', 'host', 'object', 'operation', 'process_name', 'resource', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | access |  | ['Action=({access}[^=]+?)\s*\w+='] |
| added_regex_field | action |  | ['Action=({action}[^=]+?)\s*\w+='] |
| removed_attribute | DupFields |  | N/A |