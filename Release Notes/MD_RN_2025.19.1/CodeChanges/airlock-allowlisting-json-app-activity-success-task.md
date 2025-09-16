# Code Changes for airlock-allowlisting-json-app-activity-success-task (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | result |  | ['exa_json_path=$.description,exa_regex=(\sUser:.+?\s({result}logged in))', 'exa_json_path=$.description,exa_regex=(\sUser:\s({result}Invalid login))'] |