# Code Changes for microsoft-evsecurity-json-endpoint-4768-3 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | src_host |  | ['"source":\{([^\}]*?\{([^\}]*?\{[^\{\}]*?\})*[^\}]*?\})*[^\}]*?"host":"({src_host}[^"]+)', 'workstation-name":"(-|({src_host_windows}({src_host}[^"]+)))"'] |
| edit_regex_field | src_host_windows |  | ['workstation-name":"(-|({src_host_windows}({src_host}[^"]+)))"'] |
| removed_attribute | DupFields |  | N/A |