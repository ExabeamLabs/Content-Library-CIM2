# Code Changes for okta-amfa-sk4-endpoint-login-inbounddelauth (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | additional_info |  | ['"outcome":[^\]]*?"result"\s*:\s*"(FAILURE|DENY)","reason":"({additional_info}[^"]+)', '"reason":"({additional_info}[^"]+)'] |
| removed_attribute | DupFields |  | N/A |