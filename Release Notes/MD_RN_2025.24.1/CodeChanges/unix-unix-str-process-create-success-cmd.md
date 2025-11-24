# Code Changes for unix-unix-str-process-create-success-cmd (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | account |  | ['\(({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\) CMD'] |
| edit_regex_field | user |  | ['USER = ({user}[\w\.\-\!\#\^\~]{1,40}\$?)', '\(({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\) CMD'] |
| removed_attribute | DupFields |  | N/A |