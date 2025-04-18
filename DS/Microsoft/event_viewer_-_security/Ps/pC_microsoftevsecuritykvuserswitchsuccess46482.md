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
"""Message=.+?\s({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s({domain}[^\s]+)\s({login_id}[^\s]+)\s\{([^\}]+)\}\s({dest_user}[^\s]+)\s({dest_domain}[^\s]+)\s\{.*?\}\s({dest_service_name}[^\s]+)\w.*?\s.*?\s({process_path}[^\s]+)\\({process_name}[^\s]+)""",
"""\sKeywords=({result}[^=]+?)\s\w+="""
"""\sSubjectUserName =({src_user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\sSubjectDomainName =({src_domain}[^=]+?)\s\w+="""
"""\sSubjectLogonId=({login_id}[^=]+?)\s\w+="""
"""\sTargetUserName =(SYSTEM|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""\sTargetDomainName =(NT AUTHORITY|({dest_domain}[^=]+?))\s\w+="""
"""\sTargetServerName =({dest_service_name}[^=]+?)\s\w+="""
"""\sProcessId=({process_id}[^=]+?)\s\w+="""
"""\sProcessName =({process_path}({process_dir}(?:[^"=]+)?[\\\/])?({process_name}[^\\\/"=]+?))\s\w+="""
]
DupFields = [ "host->dest_host", "src_user->user", "src_domain->domain" ]
ParserVersion = "v1.0.0"


}
```