# Code Changes for sentinelone-registry-modify-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'sentinelone-singularityp-json-registry-modify-success-regvaluemodify') && !containsAny(toLower(os), 'linux','macos','osx','win','windows') |