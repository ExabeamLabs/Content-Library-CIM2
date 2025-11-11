# Code Changes for microsoft-evsecurity-json-endpoint-login-success-4624-6 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'domain', 'host', 'process_dir', 'process_name', 'process_path', 'src_host', 'src_host_windows', 'src_ip', 'src_port', 'time', 'user', 'user_upn'] |
| edit_regex_field | host |  | ['exa_json_path=$..Computer,exa_regex=^({dest_host}({host}[\w\-.]+))$'] |
| edit_regex_field | src_host_windows |  | ["exa_json_path=$..['network_information.workstation_name'],exa_regex=^(-|({src_host_windows}({src_host}[\w\-.]+)))$"] |
| added_regex_field | dest_host |  | ['exa_json_path=$..Computer,exa_regex=^({dest_host}({host}[\w\-.]+))$'] |
| added_regex_field | src_host |  | ["exa_json_path=$..['network_information.workstation_name'],exa_regex=^(-|({src_host_windows}({src_host}[\w\-.]+)))$"] |
| removed_attribute | DupFields |  | N/A |