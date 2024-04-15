#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-delete-fail-26304740"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
"""|McAfee|ESM"""
"""43-26304740"""
]
Fields = [
"""\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|"""
"""({event_name}A user account was locked out)"""
"""\srt=({time}\d{13})"""
"""src=({host}[a-fA-F:\d.]+)"""
"""sntdom=({domain}[^\s]+)"""
"""shost=((|({domain}[^\\]*))\\+)?({src_host}[^\\\s]+)"""
"""duser=({src_user}.+?)\s+\w+="""
"""suser=({user}.+?)\s+\w+="""
"""nitroSecurity_ID=({user_sid}[^\s]+)"""
"""nitroSource_Logon_ID=({login_id}.+?)(\s|0\|)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```