# Code Changes for microsoft-evsecurity-xml-endpoint-login-fail-4625-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | failure_code |  | ['Status(:|=)\s*({result_code}({failure_code}.+?))[\s;]*Sub Status(:|=)', 'Sub Status(:|=)\s*(0x0|({result_code}({failure_code}.+?)))[\s;]*Process Information(:|=)'] |
| edit_regex_field | result_code |  | ['Status(:|=)\s*({result_code}({failure_code}.+?))[\s;]*Sub Status(:|=)', 'Sub Status(:|=)\s*(0x0|({result_code}({failure_code}.+?)))[\s;]*Process Information(:|=)'] |