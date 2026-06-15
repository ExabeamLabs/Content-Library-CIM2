# Code Changes for openai-oai-json-app-login-success-loginsucceeded (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ['epoch_sec', "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"] |
| changed_parsed_fields | N/A |  | [] |
| removed_regex_field | email_address |  | [] |
| removed_regex_field | email_domain |  | [] |
| removed_regex_field | src_ip |  | [] |
| changed | Conditions |  | ['"actor":', '"effective_at":', '"type":"login.succeeded"'] |