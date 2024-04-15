#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-4648-3"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """A logon was attempted using explicit credentials"""
  """Target Server Name"""
  """Computer"""
]
Fields = [
  """({event_name}A logon was attempted using explicit credentials)""",
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
  """<Computer>({host}[^<]+)</Computer>""",
  """Computer(\w+)?[\"\s]*(:|=)\s*\"?({host}.+?)(\"|\s|;)""",
  """({event_code}4648)""",
  """Subject(:|=)[\s;]*Security ID(:|=)\s*({user_sid}[^\s;]+?)[\s;]*Account Name(:|=)""",
  """Subject(:|=)[^\"]+?Account Name(:|=)\s*(?:-|SYSTEM|({user}[^\s;]+?))[\s;]*Account Domain(:|=)""",
  """Subject(:|=)[^\"]+?Account Domain(:|=)\s*(?:-|NT Service|({domain}[^\s;]+?))[\s;]*Logon ID(:|=)""",
  """Subject(:|=)[^\"]+?Logon ID(:|=)\s*({login_id}[^=:]+?)[\s;]*Logon GUID(:|=)""",
  """Subject(:|=)[^\"]+?Logon GUID(:|=)\s*\{({user_login_guid}[^}]+)\}[\s;]*Account Whose""",
  """Used(:|=);?\s*Account Name(:|=)\s*({dest_user}[^\s;@]+?)(@({dest_domain}[^\s;]+?))?[\s;]*Account Domain(:|=)""",
  """Used(:|=)[^\"]+?Account Domain(:|=)\s*((?i)(NULL)|({dest_domain}[^\s;]+?))[\s;]*Logon GUID(:|=)""",
  """Used(:|=)[^\"]+?Logon GUID(:|=)\s*\{({account_login_guid}[^\s;]+?)\}[\s;]*Target Server(:|=)""",
  """Target Server Name(:|=)\s*({dest_host}[^\s;]+?)(:\S+)?[\s;]*Additional Information(:|=)""",
  """Additional Information(:|=)\s*({dest_service_name}[^=:]+?)[\s;]*Process Information(:|=)""",
  """Process ID(:|=)\s*({process_id}[^=:]+?)[\s;]*Process Name(:|=)""",
  """Process Name(:|=)\s*(?:|({process_path}({process_dir}(?:[^\"]+)?[\\\/])?\s*({process_name}[^\\\/]+?)))\s+Network""",
  """Network Address(:|=)\s*(?:-|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
]
DupFields = [
"dest_user->account",
"dest_domain->account_domain"
]
ParserVersion = "v1.0.0"


}
```