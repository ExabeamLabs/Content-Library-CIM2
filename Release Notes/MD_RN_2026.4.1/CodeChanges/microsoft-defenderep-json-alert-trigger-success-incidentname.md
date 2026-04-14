# Code Changes for microsoft-defenderep-json-alert-trigger-success-incidentname (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSZ"] |
| changed_parsed_fields | N/A |  | ['alert_source'] |
| added_regex_field | alert_source |  | ['exa_regex="detectionSource":\s*"({alert_source}[^"]+)"'] |