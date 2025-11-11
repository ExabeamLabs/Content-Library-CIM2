# Code Changes for ivanti-ps-str-vpn-authentication-fail-lockedout (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account', 'dest_ip', 'dest_port', 'host', 'src_ip', 'src_port', 'time', 'user', 'vpn_client'] |
| edit_regex_field | src_ip |  | ['\d+\-\d+\-\d+\s\d+:\d+:\d+\s-\s({vpn_client}[^\s]+)\s*\-\s*\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s*[^:]+::({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | src_port |  | ['\d+\-\d+\-\d+\s\d+:\d+:\d+\s-\s({vpn_client}[^\s]+)\s*\-\s*\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s*[^:]+::({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | user |  | ['\d+\-\d+\-\d+\s\d+:\d+:\d+\s-\s({vpn_client}[^\s]+)\s*\-\s*\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s*[^:]+::({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| edit_regex_field | vpn_client |  | ['\d+\-\d+\-\d+\s\d+:\d+:\d+\s-\s({vpn_client}[^\s]+)\s*\-\s*\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s*[^:]+::({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| added_regex_field | account |  | ['\d+\-\d+\-\d+\s\d+:\d+:\d+\s-\s({vpn_client}[^\s]+)\s*\-\s*\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s*[^:]+::({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))'] |
| removed_attribute | DupFields |  | N/A |