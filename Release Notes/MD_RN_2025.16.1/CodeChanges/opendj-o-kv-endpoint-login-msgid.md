# Code Changes for opendj-o-kv-endpoint-login-msgid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "opendj-o-kv-endpoint-login-msgid", "Vendor": "OpenDJ", "Product": "OpenDJ", "TimeFormat": "dd/MMM/yyyy:HH:mm:ss Z", "Conditions": ["] BIND RES conn=", "etime=", "op=", "msgID=", "result="], "Fields": ["\[({time}\d\d\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d [-\+]\d+)\]", "conn=({connection_id}\d+)", "authFailureReason=\"({failure_reason}[^\"]+)", "authDN=\"({auth_dn}[^\"]+)", "uid=({user_uid}\d+)"], "ParserVersion": "v1.0.0"} |