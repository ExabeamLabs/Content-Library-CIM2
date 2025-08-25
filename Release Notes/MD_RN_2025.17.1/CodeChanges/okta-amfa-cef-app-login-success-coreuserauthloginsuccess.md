# Code Changes for okta-amfa-cef-app-login-success-coreuserauthloginsuccess (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | additional_info |  | ['"tunnels":"\[({additional_info}([^,]+,\\"operator\\":(null|\\"({operator_name}[^\\"]+)))?[^\]]+)', 'exa_regex="tunnels":"\[({additional_info}([^,]+,\\"operator\\":(null|\\"({operator_name}[^\\"]+)))?[^\]]+)'] |
| edit_regex_field | more_info |  | ['"behaviors\\*":"*\{({more_info}[^\}]+)', 'exa_regex=behaviors\\*":"*\{({more_info}[^\}]+)'] |