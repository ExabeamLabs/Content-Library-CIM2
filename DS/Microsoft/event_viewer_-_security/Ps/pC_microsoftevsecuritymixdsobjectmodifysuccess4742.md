#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-ds-object-modify-success-4742"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSS"]
Conditions = [
"""A computer account was changed"""
"""4742"""
]
Fields = [
"""EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
"""({event_name}A computer account was changed)"""
""""agent_hostname":"({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|({dest_host}[\w\-.]+)))""""
""""computer":"({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|({dest_host}[\w\-.]+)))"""",
"""<Computer>(::ffff:)?((?i)(am|pm)|({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-.]+)))</Computer>""",
""""ComputerName"+:"+({dest_host}({host}[\w\-\.]+))""""
"""SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+)"""
""""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
"""\srt=({time}\d{13})""",
"""({event_code}4742)"""
"""Subject:.+?\s*Account Name:\s*(\\t|\\r|\\n)*(|-|(?i)ANONYMOUS LOGON|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*(\\r|\\n|\\t)*Account Domain:\s*(\\r|\\n|\\t)*(|-|({domain}[^:]+?))(\\r|\\n|\\t)*\s*Logon ID:\s*(\\r|\\n|\\t)*(|-|({login_id}[^\s]+?))\s*(\\r|\\n|\\t)*Computer Account That Was Changed:.*?\s*Account Name:\s*(\\r|\\n|\\t)*(|-|({dest_user}[^:]+?))\s*(\\r|\\n|\\t)*Account Domain:\s*(\\r|\\n|\\t)*(|-|({ds_object_dn}[^:]+?))\s*(\\r|\\n|\\t)*Changed Attributes:"""
"""\s*Computer Account That Was Changed:.+?Account Name:\s*(\\r|\\n|\\t)*(::ffff:)?({src_host}[^$:]+?)\$(\\r|\\n|\\t)*"""
"""\s*User Principal Name:\s*(\\r|\\n|\\t)*(|-|({attribute}.+?))\s*(\\r|\\n|\\t)*Home Directory:"""
"""(?i)\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?((?i)(am|pm|\d{4})|({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-.]+)))\s"""
"""<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
"""Message(":"|>)({additional_info}[^:]+?)\s*(\\r|\\n|\\t)*\w+:"""
"""User Workstations:\s*(\\r|\\n|\\t)*(-|({src_host_windows}[^\s]+?))(\\r|\\n|\\t)*Password Last Set:"""
"""Old UAC Value:(\\t|\\r|\\n|\s)*(-|({old_value}[^":\\]+))(\\t|\\r|\\n|\s)*New UAC Value:(\\t|\\r|\\n|\s)*(-|({new_value}[^":\\]+))(\\t|\\r|\\n|\s)*User Account Control:"""
"""User Account Control:(\\t|\\r|\\n|\s)*(-|({uac_status}[^"]+))\s*(\\t|\\r|\\n|\s)*User\s*Parameters"""
"""<Data Name =\\*('|")UserAccountControl\\*('|")>(-|({uac_status}[^"<]+))<\\\/Data><Data Name =\\*"UserParameters\\*">"""
"""<Data Name =\\*('|")OldUacValue\\*('|")>(-|({old_value}[^"<]+))<\\\/Data><Data Name =\\*"NewUacValue\\*">(-|({new_value}[^"<]+))<\\\/Data><Data Name =\\*"UserAccountControl\\">"""
]
ParserVersion = "v1.0.0"


}
```