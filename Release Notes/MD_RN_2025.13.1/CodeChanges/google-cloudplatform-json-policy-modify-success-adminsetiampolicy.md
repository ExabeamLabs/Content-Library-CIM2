# Code Changes for google-cloudplatform-json-policy-modify-success-adminsetiampolicy (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | policy_bindings |  | ['"(response|request)"+:.+"+bindings"+:\s*\[\s*({policy_bindings}.+)\s*\],?[\s\]\},]+(?:"+resourceLocation"+|"+resource"+|"+@type"+|"+etag"+|"+version"+|"+serviceName"+)', 'exa_regex="response"+:.+"+bindings"+:\s*\[\s*({policy_bindings}.+)\s*\],?[\s\]\},]+(?:"+resourceLocation"+|"+resource"+|"+@type"+|"+etag"+|"+version"+|"+serviceName"+)'] |