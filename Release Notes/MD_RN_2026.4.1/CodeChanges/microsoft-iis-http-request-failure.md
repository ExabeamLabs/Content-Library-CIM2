# Code Changes for microsoft-iis-http-request-failure (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'microsoft-iis-str-http-request-get443','microsoft-iis-str-http-request-head443','microsoft-iis-str-http-request-post443','microsoft-iis-str-http-request-post80','microsoft-iis-str-http-request-head80','microsoft-iis-str-http-request-get80', 'microsoft-iis-str-http-request-headotherports', 'microsoft-iis-str-http-request-getotherports', 'microsoft-iis-str-http-request-postotherports') AND (startsWith(http_response_code, '4') OR startsWith(http_response_code, '5')) or (InList(http_response_code, '0')) |