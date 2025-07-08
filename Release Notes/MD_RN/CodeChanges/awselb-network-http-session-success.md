# Code Changes for awselb-network-http-session-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression | InList(type, 'amazon-awselb-str-http-session-elasticloadbalancing','amazon-awselb-str-http-session-elasticloadbalancing-1') && (!exists(http_response_code) OR (exists(http_response_code) AND startsWithAny(http_response_code, '1','2','3'))) | InList(type, 'amazon-awselb-str-http-session-elasticloadbalancing','amazon-awselb-str-http-session-elasticloadbalancing-1') && startsWithAny(http_response_code, '1','2','3') |