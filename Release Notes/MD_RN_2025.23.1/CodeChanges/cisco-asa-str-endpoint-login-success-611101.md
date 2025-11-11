# Code Changes for cisco-asa-str-endpoint-login-success-611101 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'email_address', 'event_code', 'event_name', 'host', 'priority', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | dest_host |  | ['\s(::ffff:)?(-|({dest_host}[\w\.-]+))[\s:]+%ASA-'] |
| removed_attribute | DupFields |  | N/A |