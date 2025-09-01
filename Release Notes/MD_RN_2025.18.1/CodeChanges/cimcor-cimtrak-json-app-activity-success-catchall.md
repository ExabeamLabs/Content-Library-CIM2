# Code Changes for cimcor-cimtrak-json-app-activity-success-catchall (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | user |  | ['exa_json_path=$.user,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)', 'exa_regex="FileUser":"\w+:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"'] |
| edit_attribute | activity_type |  | ['app-activity:fail', 'app-activity:success', 'app-authentication:success', 'app-logout:success', 'file-create:success', 'file-delete:success', 'file-write:success', 'group-member-add:success', 'group-member-remove:success', 'network-close:success'] |