# Code Changes for google-cloudplatform-json-file-permission-modify-success-storageobjectsupdatepolicydelta (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | policy_bindings |  | ['"(response|request)"+:.+"+bindings"+:\s*\[\s*({policy_bindings}.+)\s*\],?[\s\]\},]+(?:"+resourceLocation"+|"+resource"+|"+@type"+|"+etag"+|"+version"+|"+serviceName"+)'] |