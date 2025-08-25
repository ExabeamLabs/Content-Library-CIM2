# Code Changes for microsoft-evpowershell-xml-script-execute-success-4104 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | scriptblock_text |  | ['"ScriptBlockText":"({scriptblock_text}[^"]+?)\s*"', '<Data Name\\*=(\'|")ScriptBlockText(\'|")>\s*({scriptblock_text}[^<]+?)\s*<[\\\/]+Data>', 'exa_regex="ScriptBlockText":"({scriptblock_text}[^"]+?)\s*"', 'exa_regex=<Data Name\\*=(\'|")ScriptBlockText(\'|")>\s*({scriptblock_text}[^<]+?)\s*<[\\\/]+Data>'] |