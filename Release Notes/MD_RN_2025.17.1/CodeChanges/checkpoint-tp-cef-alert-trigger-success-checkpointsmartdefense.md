# Code Changes for checkpoint-tp-cef-alert-trigger-success-checkpointsmartdefense (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_name', 'alert_severity', 'alert_type', 'cve_id', 'dest_ip', 'dest_port', 'dest_user', 'dest_user_full_name', 'direction', 'domain', 'full_name', 'host', 'interface_name', 'malware_url', 'protocol', 'rule_uid', 'smartdefense_profile', 'src_host', 'src_ip', 'src_port', 'src_user', 'time', 'user_ou'] |
| added_regex_field | action |  | ['\Wact=({action}\S+)\s+'] |
| added_regex_field | cve_id |  | ['\WSignature=({cve_id}[^=]+)\s+\w+'] |
| added_regex_field | dest_user |  | ['\Wduser=({dest_user_full_name}[^(]+)\s+\(({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| added_regex_field | dest_user_full_name |  | ['\Wduser=({dest_user_full_name}[^(]+)\s+\(({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| added_regex_field | direction |  | ['\WdeviceDirection=({direction}\d+)'] |
| added_regex_field | domain |  | ['\Wshost=({src_host}[^@]+)@({domain}[^\s@]+)'] |
| added_regex_field | full_name |  | ['\Wsuser=({full_name}[^(]+)\s+\(({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |
| added_regex_field | interface_name |  | ['\Wifname=({interface_name}[^=]+)\s+\w+'] |
| added_regex_field | rule_uid |  | ['\Wrule_uid=({rule_uid}\S+)\s+'] |
| added_regex_field | smartdefense_profile |  | ['\Wsmartdefense_profile=({smartdefense_profile}[^=]+)\s+\w'] |
| added_regex_field | src_host |  | ['\Wshost=({src_host}[^@]+)@({domain}[^\s@]+)'] |
| added_regex_field | src_user |  | ['\Wsuser=({full_name}[^(]+)\s+\(({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)'] |