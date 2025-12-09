# Code Changes for crowdstrike-falcon-mix-endpoint-login-success-hostinfo (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | dest_host |  | ['"+MachineDn"+:"+CN\\*(=|u003d)?({host}({dest_host}[\w\-\.]+))', 'exa_json_path=$.MachineDn,exa_regex=CN\\*(=|u003d)?({host}({dest_host}[\w\-\.]+))'] |
| edit_regex_field | host |  | ['"+MachineDn"+:"+CN\\*(=|u003d)?({host}({dest_host}[\w\-\.]+))', '"ComputerName":"({host}[\w\-\.]+)"', 'exa_json_path=$.ComputerName,exa_regex=({host}[\w\-\.]+)', 'exa_json_path=$.MachineDn,exa_regex=CN\\*(=|u003d)?({host}({dest_host}[\w\-\.]+))'] |
| removed_attribute | DupFields |  | N/A |