# Code Changes for google-geminient-json-ai_agent-request-modelarmor (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['identifier', 'result', 'result_reason'] |
| added_regex_field | result_reason |  | ['exa_json_path=$..sanitizationResult..sanitizationVerdictReason,exa_regex=({result_reason}[^"]+)'] |