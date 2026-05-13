# Code Changes for google-geminient-json-ai_agent-request-modelarmor (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions |  | ['"sanitizationInput":', '"sanitizationResult":', '"sanitizationVerdict":', 'modelarmor.googleapis.com'] |
| changed_parsed_fields | N/A |  | ['identifier', 'result', 'result_reason'] |
| edit_regex_field | identifier |  | ['exa_json_path=$..labels.[\'modelarmor.googleapis.com/client_correlation_id\'],exa_regex=[^,"]+default_assistant\|({identifier}[^",]+)'] |
| removed_regex_field | llm_request |  | [] |