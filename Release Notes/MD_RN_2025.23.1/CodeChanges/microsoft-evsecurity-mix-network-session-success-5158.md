# Code Changes for microsoft-evsecurity-mix-network-session-success-5158 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['event_code', 'event_name', 'host', 'layer_name', 'process_dir', 'process_id', 'process_name', 'process_path', 'protocol', 'src_host', 'src_ip', 'src_port', 'time'] |
| edit_regex_field | host |  | ['Computer(Name)?\s*\\*\"?(=|:|>)\s*\"*(::ffff:)?({src_host}({host}[\w\.-]+))(\s|,|\"|</Computer>|$)', '\WComputer\\*=(::ffff:)?({host}[\w\-.]+)', '\d+\s*\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({src_host}({host}[\w\-.]+)))\s'] |
| removed_regex_field | ms_protocol_num |  | [] |
| added_regex_field | protocol |  | ['Protocol:\s*({protocol}\d*)'] |
| added_regex_field | src_host |  | ['Computer(Name)?\s*\\*\"?(=|:|>)\s*\"*(::ffff:)?({src_host}({host}[\w\.-]+))(\s|,|\"|</Computer>|$)', '\d+\s*\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({src_host}({host}[\w\-.]+)))\s'] |
| removed_attribute | DupFields |  | N/A |