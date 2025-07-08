# Code Changes for dl-netapp-netappontap-app-activity-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression | InList(type, 'netapp-netappontap-str-http-request-netapp') && (InList(toLower(result), 'pending') OR !exists(http_response_code)) | InList(type, 'netapp-netappontap-str-http-request-netapp') && InList(toLower(result), 'pending') |