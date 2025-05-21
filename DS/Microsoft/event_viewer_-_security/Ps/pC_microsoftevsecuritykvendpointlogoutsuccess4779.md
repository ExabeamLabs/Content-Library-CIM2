#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-logout-success-4779"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
"""ADAuditPlus"""
"""EVENT_NUMBER = 4779"""
"""A session was disconnected from a Window Station"""
]
Fields = [
"""TIME_GENERATED\s*=\s*({time}\d{10})"""
"""({host}[\w\-.]+) ADAuditPlus"""
"""USERNAME\s*=\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""DOMAIN\s*=\s*({domain}[^\s\]]+)"""
"""CLIENT_IP_ADDRESS\s*=\s*(LOCAL|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""CLIENT_HOST_NAME\s*=\s*(Unknown|({dest_host}[\w\-.]+))"""
"""SOURCE\s*=\s*({src_host}[\w\-.]+)"""
"""RECORD_NUMBER\s*=\s*({event_id}\d+)"""
"""EVENT_NUMBER\s*=\s*({event_code}\d+)"""
"""LOGON_ID\s*=\s*({login_id}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```