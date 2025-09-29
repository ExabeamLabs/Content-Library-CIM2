# Code Changes for crowdstrike-falcon-mix-dns-request-success-dnsrequest (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | host |  | ['"ComputerName":"({host}[\w\-\.]+)"', '"hostname":"({host}[\w\-.]+)"', 'exa_json_path=$.ComputerName,exa_regex=({host}[\w\-\.]+)', 'exa_json_path=$.hostname,exa_regex=({host}[\w\-.]+)'] |