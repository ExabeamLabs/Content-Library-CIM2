#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-mcafeeesm"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|McAfee|ESM"""
"""43-26304776"""
]
Fields = [
"""({event_name}The (computer|domain controller) attempted to validate the credentials for an account)"""
"""\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|"""
"""\srt=({time}\d{13})"""
"""src=({host}[a-fA-F:\d.]+)"""
"""nitroCommandID=({result_code}.+?)\s+\w+="""
"""The ({login_type_text}computer|domain)(\s\w+)? attempted to validate the credentials"""
"""sntdom=({domain}[^\s]+)"""
"""suser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""suser=({user_upn}[^\s]+@[^\s]+)\s+\w+="""
"""shost=({dest_host}[\w\-.]+?)\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```