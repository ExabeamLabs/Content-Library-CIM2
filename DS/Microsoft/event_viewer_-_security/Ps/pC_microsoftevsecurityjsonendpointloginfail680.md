#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-login-fail-680"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""event_id":680"""
""""Logon attempt by:"""
""""@timestamp""""
]
Fields = [
"""({event_name}Logon attempt)"""
""""@timestamp"\s*:\s*"({time}[^"]+)""""
""""(?:winlog\.)?computer_name"\s*:\s*"({host}[\w\-\.]+)""""
""""event_data"\s*:\s*\{.*?"(param3|SourceWorkstation)"\s*:\s*"({dest_host}[^"]+)""""
""""event_data"\s*:\s*\{.*?"(param4|ErrorCode)"\s*:\s*"({result_code}[^"]+)""""
""""event_data"\s*:\s*\{.*?"(param2|UserName|User)"\s*:\s*"({user}[^"]+)""""
""""hostname":"({domain}[^"]+)""""
""""user"\s*:\s*\{.*?"identifier"\s*:\s*"({user_sid}[^"]+)""""
""""user"\s*:\s*\{.*?"domain":"({domain}[^"]+)""""
""""user"\s*:\s*\{.*?"name":"({user}[^"]+)""""
""""event_id"\s*:\s*({event_code}\d+)"""
""""record_number"\s*:\s*"({event_id}\d+)"""
]
DupFields = [
  "result_code->failure_code"
]
ParserVersion = "v1.0.0"


}
```