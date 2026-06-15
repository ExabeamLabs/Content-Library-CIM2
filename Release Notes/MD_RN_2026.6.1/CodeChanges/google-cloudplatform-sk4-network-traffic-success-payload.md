# Code Changes for google-cloudplatform-sk4-network-traffic-success-payload (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| COULD_NOT_COMPARE | TimeFormat |  | ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSZ"] |
| changed_parsed_fields | N/A |  | ['action', 'bytes_out', 'dest_ip', 'dest_port', 'direction', 'host', 'packets', 'protocol', 'reporter', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | action |  | ['"disposition":"({action}[^"]+)"'] |
| edit_attribute | activity_type |  | ['network-traffic:fail', 'network-traffic:success'] |
| edit_attribute | legacy_activity_type |  | ['netflow-connection', 'network-connection-failed'] |