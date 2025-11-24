# Code Changes for absolute-siemconnector-cef-app-activity-success-deviceuserinformationupdated (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'email_user', 'event_name', 'host', 'object', 'operation', 'src_host', 'time', 'user'] |
| edit_regex_field | operation |  | ['({event_name}({operation}DeviceUserInformationUpdated))'] |
| added_regex_field | event_name |  | ['({event_name}({operation}DeviceUserInformationUpdated))'] |
| removed_attribute | DupFields |  | N/A |