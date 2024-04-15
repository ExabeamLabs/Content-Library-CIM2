#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-delete-success-4743-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""A computer account was deleted"""
"""4743"""
"""(EventID 4743)"""
"""Microsoft Windows security auditing"""
]
Fields = [
"""({event_name}A computer account was deleted)"""
"""({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+({event_code}\d+)"""
"""({event_code}4743)"""
""":\d+:\d+\s+(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({host}[\w\-.]+))\s+MSWinEventLog"""
"""Security ID:\s+(NT AUTHORITY\\(SYSTEM|LOCAL SERVICE)|({user_sid}[^:]+?))\s+Account Name:\s+(?=\w)({user}[^:]+?)\s+Account Domain:\s+(?=\w)({domain}[^:]+?)\s+Logon ID:\s+({login_id}[^\s]+)\s+"""
"""Target Computer:\s+Security ID:\s+(NT AUTHORITY\\(SYSTEM|LOCAL SERVICE)|({dest_user_sid}[^:]+?))\s+Account Name:\s+(?=\w)({dest_user}[^:]+?)\s+Account Domain:\s+(?=\w)({object_dn}[^:]+?)\s+Additional Information:"""
]
DupFields = [
"host->dest_host"
"dest_user->object"
]
ParserVersion = "v1.0.0"


}
```