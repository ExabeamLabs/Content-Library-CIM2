# Code Changes for dl-checkpoint-network-http-session-success-1 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'checkpoint-ngfw-kv-http-session-ifname','checkpoint-ngfw-kv-http-session-url','checkpoint-ngfw-kv-http-session-urlfilter','checkpoint-ngfw-kv-http-session-filtering') && InList(ToLower(action),'allow','accept') && !(exists(web_domain) || (exists(category) && category='Web Advertisements')) |