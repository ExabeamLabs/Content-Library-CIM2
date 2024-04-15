#### Parser Content
```Java
{
Name = "microsoft-evapplocker-cef-endpoint-notification-8002-tl"
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Event Viewer - Applocker"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""eventid":8002"""
"""a process was allowed to run"""
]
Fields = [
"""(?i)"Activity":"(\d+\s+-\s+)?({event_name}[^"]+?)""""
"""(?i)"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""(?i)"Computer":"({host}[^"]+)"""
"""(?i)"EventID":"?({event_code}\d+)"""
"""(?i)"Account":"(({domain}[^\\"]+)\\+)?({user}[^\\"]+)"""
"""(?i)<TargetLogonId>({login_id}.+?)</TargetLogonId>"""
"""(?i)"TargetLogonId":"({login_id}[^"]+)"""
"""(?i)"TargetUserSid":"({user_sid}[^"]+)"""
"""(?i)"TargetUser":"({user}[^"]+)"""
"""(?i)"FileHash":"({hash_md5}[^"]+)"""
"""(?i)"FilePath":"({file_path}({file_dir}[^"]*?[\\\/]+)?({file_name}[^"\\\/]+?(\.({file_ext}[^"\.\\\/]+))?))""""
# fqbn is removed
"""(?i)"Process":"({process_name}[^"]+)"""
]


}
```