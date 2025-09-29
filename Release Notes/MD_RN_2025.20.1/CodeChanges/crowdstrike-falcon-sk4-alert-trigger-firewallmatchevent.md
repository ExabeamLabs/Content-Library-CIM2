# Code Changes for crowdstrike-falcon-sk4-alert-trigger-firewallmatchevent (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'cid', 'dest_ip', 'dest_port', 'direction', 'event_name', 'file_dir', 'file_ext', 'file_name', 'host', 'policy_name', 'process_command_line', 'protocol', 'rule', 'src_ip', 'src_port', 'time'] |
| added_regex_field | file_dir |  | ['"(ImageFileName|TargetFileName)":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?(\.(\d+|({file_ext}\w{1,10}?)))?)\s*"', 'exa_regex="(ImageFileName|TargetFileName)":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?(\.(\d+|({file_ext}\w{1,10}?)))?)\s*"'] |
| added_regex_field | file_ext |  | ['"(ImageFileName|TargetFileName)":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?(\.(\d+|({file_ext}\w{1,10}?)))?)\s*"', 'exa_regex="(ImageFileName|TargetFileName)":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?(\.(\d+|({file_ext}\w{1,10}?)))?)\s*"'] |
| added_regex_field | file_name |  | ['"(ImageFileName|TargetFileName)":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?(\.(\d+|({file_ext}\w{1,10}?)))?)\s*"', 'exa_regex="(ImageFileName|TargetFileName)":\s*"({file_dir}[^"]*[\\\/]+)({file_name}[^\\\/"]+?(\.(\d+|({file_ext}\w{1,10}?)))?)\s*"'] |
| added_regex_field | process_command_line |  | ['"CommandLine":"({process_command_line}[^"]+)"'] |