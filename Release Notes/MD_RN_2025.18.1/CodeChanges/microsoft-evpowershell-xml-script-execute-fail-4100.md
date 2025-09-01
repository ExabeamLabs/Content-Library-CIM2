# Code Changes for microsoft-evpowershell-xml-script-execute-fail-4100 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | failure_reason |  | ['Data Name=(\'|")Payload(\'|")>Error Message = ({failure_reason}[^<]+?)\s*<'] |
| edit_regex_field | user_sid |  | ['<Security UserID=(\'|")({user_sid}[^\'<"]+)'] |