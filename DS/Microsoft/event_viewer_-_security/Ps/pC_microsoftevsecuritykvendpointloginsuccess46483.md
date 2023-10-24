#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-4648-3"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss", "epoch_sec", "MM/dd/yyyy hh:mm:ss a"]
Conditions = [
  """A logon was attempted using explicit credentials"""
  """Target Server Name"""
  """Computer"""
]
Fields = [
  """({event_name}A logon was attempted using explicit credentials)""",
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
  """TimeGenerated=({time}\d{10})"""
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
  """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
  """Computer(\w+)?[\"\s]*(:|=)\s*\"?({dest_host}({host}[\w\-.]+?))(\"|\s|;)""",
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
  """({event_code}4648)""",
  """Account Whose Credentials Were Used:.+?Account Name(:|=)\s*(-|SYSTEM|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+(?<!local)(?<!loc))\s|({user}[\w\.\-]{1,40}\$?)))"""
  """Subject(:|=)[\s;]*Security ID(:|=)\s*({user_sid}[^\s;]+?)[\s;]*Account Name(:|=)""",
  """Subject(:|=).+?Account Name(:|=)\s*(\\t|\\r|\\n)*(?:-|SYSTEM|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^<\]\s"\\,\|]+(?<!local)(?<!loc))|({user}[\w\.\-]{1,40}\$?)))[\s;]+(\\t|\\r|\\n)*Account Domain(:|=)""",
  """Subject(:|=)[^\"]+?Account Domain(:|=)\s*(\\t)?(?:-|NT Service|({domain}[^\s;]+?))[\s;]*(\s*\\r\s\\t)?Logon ID(:|=)""",
  """Subject(:|=)[^\"]+?Logon ID(:|=)\s*({login_id}[^=:]+?)[\s;]*Logon GUID(:|=)""",
  """Subject(:|=)[^\"]+?Logon GUID(:|=)\s*\{({user_login_guid}[^}]+)\}[\s;]*Account Whose""",
  """Used(:|=);?\s*Account Name(:|=)\s*({dest_user}[^\s;@]+?)(@({dest_domain}[^\s;]+?))?[\s;]*Account Domain(:|=)""",
  """Used(:|=)[^\"]+?Account Domain(:|=)\s*((?i)(NULL)|({dest_domain}[^\s;]+?))[\s;]*Logon GUID(:|=)""",
  """Used(:|=)[^\"]+?Logon GUID(:|=)\s*\{({account_login_guid}[^\s;]+?)\}[\s;]*Target Server(:|=)""",
  """Target Server Name(:|=)\s*({dest_host}[\w\-.]+?)(:\S+)?[\s;]*Additional Information(:|=)""",
  """Additional Information(:|=)\s*({dest_service_name}[^=:]+?)[\s;]*Process Information(:|=)""",
  """Process ID(:|=)\s*({process_id}[^=:]+?)[\s;]*Process Name(:|=)""",
  """Process Name(:|=)\s*(?:|({process_path}({process_dir}(?:[^\"]+)?[\\\/])?\s*({process_name}[^\\\/]+?)))\s+Network""",
  """Network Address(:|=)\s*(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
  """Account Name:\s*([\\t]*)?(-|({account}.+?))\s*(\\r|\\t|\\n)*?\s*Account Domain:"""
]
DupFields = [
"dest_user->account",
"dest_domain->account_domain"
]
ParserVersion = "v1.0.0"


}
```