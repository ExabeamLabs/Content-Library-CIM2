# Code Changes for amazon-awscloudtrail-json-disk-modify-modifyvolume (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | readonly |  | ['"readOnly"\s*:\s*"?({readonly}[^",\}]+)("|,|\}\s*$)'] |