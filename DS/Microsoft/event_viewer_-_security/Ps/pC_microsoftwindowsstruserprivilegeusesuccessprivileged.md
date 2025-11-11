#### Parser Content
```Java
{
Name = "microsoft-windows-str-user-privilege-use-success-privileged"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""     578     """
"""Privileged object operation:"""
]
Fields = [
"""({event_name}Privileged object operation)"""
"""\s+(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)\s+"""
"""\s+(Information|Audit Success|Success Audit)\s+({dest_host}({host}[\w\-.]+))"""
"""(?:Information|Audit Success|Success Audit).+?Primary User Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Primary Domain"""
"""({event_code}578)"""
"""Security\t([^\s]+\t){2}({result}.+?)\t"""
"""\s+Primary Domain:\s+({domain}[^\s]+)"""
"""\s+Primary Logon ID:\s+\([^,]+,({login_id}[^)]+)"""
"""\s+Object Server:\s+(?:-|({object_server}.+?))\s+Object Handle"""
"""\s+Privileges:\s+({privileges}.+?)\s+\d+"""
"""\s+({ownership_privilege}SeTakeOwnershipPrivilege)"""
"""\s+({environment_privilege}SeSystemEnvironmentPrivilege)"""
"""\s+({debug_privilege}SeDebugPrivilege)"""
"""\s+({tcb_privilege}SeTcbPrivilege)"""
]
ParserVersion = "v1.0.0"


}
```