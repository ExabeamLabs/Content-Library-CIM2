#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-switch-success-4648-1"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss yyyy"]
  Conditions = [
"""A logon was attempted using explicit credentials""",
"""Target Server Name"""
  ]
  Fields = [
"""({event_name}A logon was attempted using explicit credentials)""",
"""hostname=({host}[\w\-\.]+),\s*\w+=""",
""""hostname":"({host}[\w\.\-]+)""""
"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
"""\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
"""({time}\w+\s\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s\d{4})\s+\d+\s+Microsoft-Windows-Security-Auditing""",
"""(?i)\w+\s*\d+\s\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({host}[\w\-.]+))\s+[a-zA-Z]+""",
"""(?i)\w+\s*\d+\s\d+:\d+:\d+\s+(::ffff:)?(am|pm|({host}[\w\-.]+))\s+[a-zA-Z]+""",
"""({event_code}4648)""",
"""Subject(:|=)[\s;]*(\\t|\\r|\\n)*Security ID(:|=)\s*(\\t|\\r|\\n)*({user_sid}S-.*?)[\s;]*(\\t|\\r|\\n)*Account Name(:|=)""",
"""Subject(:|=).+?Account Name(:|=)\s*(\\t|\\r|\\n)*(?:-|SYSTEM|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))[\s;]*(\\t|\\r|\\n)*Account Domain(:|=)""",
"""Subject(:|=).+?Account Domain(:|=)\s*(\\t|\\r|\\n)*(?:-|NT Service|({domain}[^\s]*?))[\s;]*(\\t|\\r|\\n)*Logon ID(:|=)""",
"""Subject(:|=).+?Logon ID(:|=)\s*(\\r|\\t|\\n)*({login_id}.*?)[\s;]*(\\r|\\t|\\n)*Logon GUID(:|=)""",
"""Subject(:|=).+?Logon GUID(:|=)\s*(\\r|\\t|\\n)*\{({user_login_guid}[^}]+)\}[\s;]*(\\r|\\t|\\n)*Account Whose""",
"""Used(:|=);?\s*(\\r|\\t|\\n)*Account Name(:|=)\s*(\\r|\\t|\\n)*(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))[\s;]*(\\r|\\t|\\n)*Account Domain(:|=)""",
"""Used(:|=).+?Account Domain(:|=)\s*(\\r|\\t|\\n)*(|({dest_domain}.*?))[\s;]*(\\r|\\t|\\n)*Logon GUID(:|=)""",
"""Used(:|=).+?Logon GUID(:|=)\s*(\\r|\\t|\\n)*\{({account_login_guid}.*?)\}[\s;]*(\\r|\\t|\\n)*Target Server(:|=)""",
"""Target Server Name(:|=)\s*(\\t|\\r|\\n)*(::ffff:)?({dest_host}[\w\-.]*?\$?)[\s;]*(\\t|\\r|\\n)*Additional Information(:|=)""",
"""Additional Information(:|=)\s*(\\r|\\t|\\n)*({dest_service_name}.*?)[\s;]*(\\r|\\t|\\n)*(Network Information|Process Information|\w+=)""",
"""Process ID(:|=)\s*(\\r|\\t|\\n)*({process_id}.*?)[\s;]*(\\r|\\t|\\n)*Process Name(:|=)""",
"""Process Name(:|=)\s*(\\r|\\t|\\n)*(?: |({process_path}({process_dir}(\w+:)(?:[^\";]+)?[\\\/])?({process_name}[^\\\/\";]+?)))[\s;]*Network Information(:|=)""",
"""Network Address(:|=)\s*(?:-|(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
""""source_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""  
]
DupFields = [
"dest_user->account",
"dest_domain->account_domain"
]


}
```