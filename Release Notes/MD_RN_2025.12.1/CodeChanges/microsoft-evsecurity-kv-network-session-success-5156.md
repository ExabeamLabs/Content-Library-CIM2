# Code Changes for microsoft-evsecurity-kv-network-session-success-5156 (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| edit_regex_field | process_dir | ['Application Name:\s*({process_path}({process_dir}.+?)[\\\/]({process_name}.+?))\s*Network Information:'] | ['Application Name:\s*({process_path}({process_dir}.+?)[\\\/]({process_name}[^\\\/]+?))\s*Network Information:'] |
| edit_regex_field | process_name | ['Application Name:\s*({process_path}({process_dir}.+?)[\\\/]({process_name}.+?))\s*Network Information:'] | ['Application Name:\s*({process_path}({process_dir}.+?)[\\\/]({process_name}[^\\\/]+?))\s*Network Information:'] |
| edit_regex_field | process_path | ['Application Name:\s*({process_path}({process_dir}.+?)[\\\/]({process_name}.+?))\s*Network Information:'] | ['Application Name:\s*({process_path}({process_dir}.+?)[\\\/]({process_name}[^\\\/]+?))\s*Network Information:'] |