#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-4769-10"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""ADAuditPlus"""
"""EVENT_NUMBER = 4769"""
"""A Kerberos service ticket was requested"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+\-]\d\d:\d\d)\s+({host}[\w\-.]+)\s+ADAuditPlus"""
"""({event_name}A Kerberos service ticket was requested)"""
"""({event_code}4769)"""
"""USERNAME\s*=\s*(null|-|({user}[\w\.\-]{1,40}\$?))(@({domain}[^@\s]+))?\s"""
"""DOMAIN\s*=\s*(null|-|({domain}[^\s\]]+))"""
"""CLIENT_IP_ADDRESS\s*=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""CLIENT_HOST_NAME\s*=\s*({src_host}[\w\-.]+)"""
"""LOGON_SERVICE\s*=\s*(null|-|({service_name}[^\s\]]+))"""
"""ERROR_CODE\s*=\s*(null|-|({result_code}[^\s\]]+))"""
"""TICKET_OPTIONS\s*=\s*(null|-|({ticket_options}[^\s\]]+))"""
"""TICKET_ENCRYPTION_TYPE\s*=\s*(null|-|({ticket_encryption_type}[^\s\]]+))"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```