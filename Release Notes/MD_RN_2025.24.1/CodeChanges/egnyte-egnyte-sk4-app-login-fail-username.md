# Code Changes for egnyte-egnyte-sk4-app-login-fail-username (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'category', 'dproc', 'email_address', 'email_domain', 'event_name', 'event_subtype', 'full_name', 'operation', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | dproc |  | ['dproc=({category}({dproc}[^=]+))\s\w+='] |
| added_regex_field | category |  | ['dproc=({category}({dproc}[^=]+))\s\w+='] |
| removed_attribute | DupFields |  | N/A |