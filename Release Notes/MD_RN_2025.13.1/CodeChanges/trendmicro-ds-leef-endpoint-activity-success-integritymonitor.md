# Code Changes for trendmicro-ds-leef-endpoint-activity-success-integritymonitor (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | process_dir |  | ['sproc=(N\/A|({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?)))\sentityType='] |
| edit_regex_field | process_name |  | ['sproc=(N\/A|({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?)))\sentityType='] |
| edit_regex_field | process_path |  | ['sproc=(N\/A|({process_path}({process_dir}[^=]*[\\\/]+)?({process_name}[^=]+?)))\sentityType='] |