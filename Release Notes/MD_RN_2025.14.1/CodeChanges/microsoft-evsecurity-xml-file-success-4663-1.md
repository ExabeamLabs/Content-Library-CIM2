# Code Changes for microsoft-evsecurity-xml-file-success-4663-1 (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['access', 'access_mask', 'domain', 'event_code', 'file_dir', 'file_type', 'host', 'login_id', 'process_dir', 'process_name', 'process_path', 'registry_key', 'registry_path', 'run_level', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_host', 'time', 'user', 'user_sid'] | ['access', 'access_mask', 'domain', 'event_code', 'file_dir', 'file_ext', 'file_name', 'file_path', 'file_type', 'host', 'login_id', 'process_dir', 'process_name', 'process_path', 'registry_key', 'registry_path', 'run_level', 'src_host', 'time', 'user', 'user_sid'] |
| edit_regex_field | registry_key | ['<Data Name\\*="ObjectName">(({registry_path}\\+REGISTRY[^<]+?({registry_key}[^\\\/<]+))|({src_file_path}[^<]+))<'] | ['<Data Name\\*="ObjectName">(({registry_path}\\+REGISTRY[^<]+?({registry_key}[^\\\/<]+))|({file_path}[^<]+))<'] |
| edit_regex_field | registry_path | ['<Data Name\\*="ObjectName">(({registry_path}\\+REGISTRY[^<]+?({registry_key}[^\\\/<]+))|({src_file_path}[^<]+))<'] | ['<Data Name\\*="ObjectName">(({registry_path}\\+REGISTRY[^<]+?({registry_key}[^\\\/<]+))|({file_path}[^<]+))<'] |
| removed_regex_field | src_file_ext | ['<Data Name\\*="ObjectName">(?!\\+REGISTRY)[^<]+[\\\/]+({src_file_name}(?:[^<\\\/:]+?)(\.({src_file_ext}\w+))?|[^\\:<]+)<'] | [] |
| removed_regex_field | src_file_name | ['<Data Name\\*="ObjectName">(?!\\+REGISTRY)[^<]+[\\\/]+({src_file_name}(?:[^<\\\/:]+?)(\.({src_file_ext}\w+))?|[^\\:<]+)<'] | [] |
| removed_regex_field | src_file_path | ['<Data Name\\*="ObjectName">(({registry_path}\\+REGISTRY[^<]+?({registry_key}[^\\\/<]+))|({src_file_path}[^<]+))<'] | [] |
| added_regex_field | file_ext | [] | ['<Data Name\\*="ObjectName">(?!\\+REGISTRY)[^<]+[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?|[^\\:<]+)<'] |
| added_regex_field | file_name | [] | ['<Data Name\\*="ObjectName">(?!\\+REGISTRY)[^<]+[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?|[^\\:<]+)<'] |
| added_regex_field | file_path | [] | ['<Data Name\\*="ObjectName">(({registry_path}\\+REGISTRY[^<]+?({registry_key}[^\\\/<]+))|({file_path}[^<]+))<'] |