# Code Changes for cisco-tacacs-kv-process-create-success-tacacs (Parser)

| Code Change | Field Name | 2025.14.1 | 2025.15.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "cisco-tacacs-kv-process-create-success-tacacs", "Vendor": "Cisco", "Product": "Cisco Identity and Access Management", "TimeFormat": "epoch_sec", "Conditions": ["[TACACS]", "start_time=", "cmd="], "Fields": ["\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s+\S+\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\S+\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+", "start_time=({time}\d{10})", "cmd=\S+\s+({process_command_line}.+?)\s*$", "cmd=\S+\s+({process_name}[^\s]+)"], "ParserVersion": "v1.0.0"} | N/A |