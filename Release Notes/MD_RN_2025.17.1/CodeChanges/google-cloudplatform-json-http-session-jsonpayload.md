# Code Changes for google-cloudplatform-json-http-session-jsonpayload (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | TimeFormat |  | yyyy-MM-dd'T'HH:mm:ss |
| changed | Conditions |  | ['"gce_instance"', '"jsonPayload":', '"project_id":', 'googleapis.com', 'resource_name":'] |
| changed_parsed_fields | N/A |  | ['action', 'dest_ip', 'dest_port', 'src_ip', 'src_port', 'time'] |
| added_regex_field | time |  | ['exa_regex=timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)'] |