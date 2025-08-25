# Code Changes for google-cloudplatform-json-scheduled-success-scheduler (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"] |
| edit_regex_field | event_name |  | ['"@type":".+?({event_name}scheduler[^"]+)"', 'exa_regex=@type":".+?({event_name}scheduler[^"]+)"'] |
| added_attribute | ExtractionType |  | json |