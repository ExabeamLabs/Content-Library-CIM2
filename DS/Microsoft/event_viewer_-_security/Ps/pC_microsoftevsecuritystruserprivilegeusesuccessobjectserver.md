#### Parser Content
```Java
{
Name = "microsoft-evsecurity-str-user-privilege-use-success-objectserver"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
ParserVersion = "v1.0.0"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """Microsoft-Windows-Security-Auditing""", """PrivilegeList:""", """4674""", """ObjectServer:""", """Sensitive Privilege Use""", """AccessMask:""", """HandleId:""" ]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d{1,3}[+\-]+\d\d:\d\d""",
"""({host}[\w\-.]+)\s+Sensitive Privilege Use""",
"""({event_code}4674)""",
"""SubjectUserName:({user}[\w\.\-]{1,40}\$?),""",
"""SubjectDomainName:({domain}[^,]+),""",
"""SubjectLogonId:({login_id}[^,]+),""",
"""PrivilegeList:({privileges}[^:]+),\s+\w+:""",
"""ProcessId:({process_id}[^,]+),""",
"""ProcessName:({process_path}(({process_dir}[^"]+)[\\\/])?({process_name}[^"\\]+?))\s+\d+""",
"""({result}(Success|Failure) Audit)"""
"""ObjectServer:({object_server}[^,]+),""",
"""ObjectName:(-|({object}[^,]+)),""",
"""HandleId:({handle_id}[^,]+),"""
]
DupFields = ["host->dest_host"]


}
```