#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-switch-success-4648-1"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""A logon was attempted using explicit credentials""",
"""Target Server Name"""
  ]
  Fields = [
"""({event_name}A logon was attempted using explicit credentials)""",
"""hostname=({host}[^=]+?),\s*\w+=""",
"""({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
"""(?i)\w+\s*\d+\s\d+:\d+:\d+\s+(::ffff:)?(am|pm|({host}[\w\-.]+))""",
"""({event_code}4648)""",
"""Subject(:|=)[\s;]*Security ID(:|=)\s*({user_sid}.*?)[\s;]*Account Name(:|=)""",
"""Subject(:|=).+?Account Name(:|=)\s*(?:-|SYSTEM|({user}[^\s]*?))[\s;]*Account Domain(:|=)""",
"""Subject(:|=).+?Account Domain(:|=)\s*(?:-|NT Service|({domain}[^\s]*?))[\s;]*Logon ID(:|=)""",
"""Subject(:|=).+?Logon ID(:|=)\s*({login_id}.*?)[\s;]*Logon GUID(:|=)""",
"""Subject(:|=).+?Logon GUID(:|=)\s*\{({user_login_guid}[^}]+)\}[\s;]*Account Whose""",
"""Used(:|=);?\s*Account Name(:|=)\s*({dest_user}.*?)[\s;]*Account Domain(:|=)""",
"""Used(:|=).+?Account Domain(:|=)\s*(|({dest_domain}.*?))[\s;]*Logon GUID(:|=)""",
"""Used(:|=).+?Logon GUID(:|=)\s*\{({account_login_guid}.*?)\}[\s;]*Target Server(:|=)""",
"""Target Server Name(:|=)\s*(::ffff:)?({dest_host}.*?)[\s;]*Additional Information(:|=)""",
"""Additional Information(:|=)\s*({dest_service_name}.*?)[\s;]*Process Information(:|=)""",
"""Process ID(:|=)\s*({process_id}.*?)[\s;]*Process Name(:|=)""",
"""Process Name(:|=)\s*(?: |({process_path}({process_dir}(\w+:)(?:[^\";]+)?[\\\/])?({process_name}[^\\\/\";]+?)))[\s;]*Network Information(:|=)""",
"""Network Address(:|=)\s*(?:-|(::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  ]
DupFields = [
"dest_user->account",
"dest_domain->account_domain"
]


}
```