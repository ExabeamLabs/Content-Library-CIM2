# Code Changes for juniper-jn-kv-app-login-fail-sshdloginfailed (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['dest_host', 'host', 'src_ip', 'src_port', 'time', 'user'] |
| edit_regex_field | host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\-|\+)\d\d:\d\d) ({dest_host}({host}[\w\-.]+)) sshd - SSHD_LOGIN_FAILED'] |
| edit_regex_field | time |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\-|\+)\d\d:\d\d) ({dest_host}({host}[\w\-.]+)) sshd - SSHD_LOGIN_FAILED'] |
| added_regex_field | dest_host |  | ['({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\-|\+)\d\d:\d\d) ({dest_host}({host}[\w\-.]+)) sshd - SSHD_LOGIN_FAILED'] |
| removed_attribute | DupFields |  | N/A |