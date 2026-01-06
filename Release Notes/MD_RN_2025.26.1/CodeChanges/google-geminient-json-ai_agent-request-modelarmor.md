# Code Changes for google-geminient-json-ai_agent-request-modelarmor (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['identifier', 'llm_request', 'result', 'result_reason'] |
| added_regex_field | llm_request |  | ['exa_json_path=$..sanitizationInput.text,exa_regex=({llm_request}.{0,256})'] |