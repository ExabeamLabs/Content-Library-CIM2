# Code Changes for checkpoint-network-http-session-fail (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'checkpoint-ngfw-kv-http-session-ifname','checkpoint-ngfw-kv-http-session-url','checkpoint-ngfw-kv-http-session-urlfilter','checkpoint-ngfw-kv-http-session-filtering') && exists(web_domain) && !InList(ToLower(action),'allow','accept') && not (exists(category) && category='Web Advertisements') |