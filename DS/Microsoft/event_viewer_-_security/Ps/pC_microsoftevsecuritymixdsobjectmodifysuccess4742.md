#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-ds-object-modify-success-4742"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
"""A computer account was changed"""
"""4742"""
]
Fields = [
"""EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
"""({event_name}A computer account was changed)"""
""""agent_hostname":"({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|({dest_host}[^"]+)))""""
""""computer":"({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|({dest_host}[^"]+)))"""",
"""<Computer>(::ffff:)?((?i)(am|pm)|({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^<]+)))</Computer>""",
"""SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)"""
"""({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+)"""
"""({event_code}4742)"""
"""Subject:.+?\sAccount Name:\s*(|-|({user}[^:]+?))\s*Account Domain:\s*(|-|({domain}[^:]+?))\s*Logon ID:\s*(|-|({login_id}[^\s]+))\s*Computer Account That Was Changed:.*?\sAccount Name:\s*(|-|({dest_user}[^:]+?))\s*Account Domain:\s*(|-|({object_dn}[^:]+?))\s*Changed Attributes:"""
"""\sComputer Account That Was Changed:.+?Account Name:\s*(::ffff:)?({src_host}[^$:]+?)\$"""
"""\sUser Principal Name:\s*(|-|({attribute}.+?))\s*Home Directory:"""
"""(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?((?i)(am|pm)|({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-.]+)))\s"""
"""Message(":"|>)({additional_info}[^:]+?)\s*\w+:"""
"""User Workstations:\s*(-|({src_host_windows}[^\\\s]+))\s*"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```