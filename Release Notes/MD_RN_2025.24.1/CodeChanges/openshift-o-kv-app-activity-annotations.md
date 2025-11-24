# Code Changes for openshift-o-kv-app-activity-annotations (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | object |  | ['"resource\\?":\\?"({object}({resource}[^"\\]+))', 'resource\\xAE({object}[^\\]+)'] |
| edit_regex_field | resource |  | ['"resource\\?":\\?"({object}({resource}[^"\\]+))'] |
| removed_attribute | DupFields |  | N/A |