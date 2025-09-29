# Code Changes for crowdstrike-falcon-json-network-traffic-success-connectip (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['"ComputerName":"({host}[\w\-\.]+)"', 'exa_json_path=$.ComputerName,exa_regex=({host}[\w\-\.]+)', 'hostname":"({host}[^"]+)"'] |