# Code Changes for azure-app-notificatation-json (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['additional_info', 'event_name', 'object', 'operation', 'provider_name', 'resource', 'resource_group', 'resource_id', 'subscription_id', 'time'] |
| edit_regex_field | object |  | ['"resourceId":"({resource}({object}[^"]+))"', '"resourceProviderName":\{.+?resourceId":"({resource}({object}[^"]+))"'] |
| added_regex_field | resource |  | ['"resourceId":"({resource}({object}[^"]+))"', '"resourceProviderName":\{.+?resourceId":"({resource}({object}[^"]+))"'] |
| removed_attribute | DupFields |  | N/A |