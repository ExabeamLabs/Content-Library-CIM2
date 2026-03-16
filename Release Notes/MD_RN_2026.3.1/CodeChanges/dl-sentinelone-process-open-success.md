# Code Changes for dl-sentinelone-process-open-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'sentinelone-singularityp-json-process-open-success-processopen') && !containsAny(toLower(os), 'linux','macos','osx','win','windows') |