# Code Changes for microsoft-evpowershell-xml-process-create-success-4103-1 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | command_module |  | ['Details:.+?CommandInvocation.+?ParameterBinding.+?value=\\"(function\s)?({command_module}[^\s\\,"]+)', 'value="*(?:function\s)?({command_module}[^\s"]+)'] |