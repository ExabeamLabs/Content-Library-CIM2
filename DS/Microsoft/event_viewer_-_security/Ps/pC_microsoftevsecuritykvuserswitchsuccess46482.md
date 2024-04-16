#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-switch-success-4648-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
"""EventIDCode=4648"""
]
Fields = [
"""TimeGenerated=({time}\d{10})"""
"""EventIDCode=({event_code}\d+)"""
"""\s+Computer=({host}[\w.\-]+)"""
"""Message=.+?\s({user}[\w\.\-]{1,40}\$?)\s({domain}[^\s]+)\s({login_id}[^\s]+)\s\{([^\}]+)\}\s({dest_user}[^\s]+)\s({dest_domain}[^\s]+)\s\{.*?\}\s({dest_service_name}[^\s]+)\w.*?\s.*?\s({process_path}[^\s]+)\\({process_name}[^\s]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```