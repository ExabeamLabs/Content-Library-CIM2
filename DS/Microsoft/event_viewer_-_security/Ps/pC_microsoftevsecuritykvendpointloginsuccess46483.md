#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-4648-3"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss", "epoch_sec", "MM/dd/yyyy hh:mm:ss a", "yyyy-MM-dd HH:mm:ss Z"]
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
  """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\d(T|\s)\d\d:\d\d:\d\d(\s*(\+|\-)[\d\:]+)?)"""",
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d\s*({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w.\-]+))"""
  """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
  """Computer(\w+)?[\"\s]*(:|=)\s*\"?({dest_host}({host}[\w\-.]+?))(\"|\s|;)""",
  """({event_code}4648)""",
  """Account Whose Credentials Were Used:.+?Account Name(:|=)[\\t\s]*(-|SYSTEM|(({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+(?<!local)(?<!loc))\s|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))[\\r\\t\\n]*\s*(\w+\s\w+:|\w+=|[\w\s]+?\.)"""
  """Subject(:|=).+?Security ID(:|=)[\\t\s]*({user_sid}NULL SID|S-[^\:]+?)[;\s\\n\\r\\t]*\w+\s\w+(:|=)""",
  """Subject(:|=).+?Account Name(:|=)\s*(\\t|\\r|\\n)*(?:-|SYSTEM|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^<\]\s"\\,\|]+(?<!local)(?<!loc))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))[\s;]*(\\t|\\r|\\n)*(Account Domain(:|=)|\w+=|[\w\s]+?\.)""",
  """Subject(:|=)[^\"]+?Account Domain(:|=)\s*(\\r|\\n|\\t)*(?:-|NT Service|({domain}[^\s;]+?))[\s;]*(\\r|\\n|\\t)*Logon ID(:|=)""",
  """Subject(:|=)[^\"]+?Logon ID(:|=)\s*(\\t)*({login_id}[^=:;\s;\\]+)[\s;]*""",
  """Subject(:|=)[^\"]+?Logon GUID(:|=)(\\[rnt]|\s)*\{({user_login_guid}[^}]+)\}[\s;]*(\\[rnt]|\s)*Account Whose""",
  """Used(:|=);?\s*Account Name(:|=)\s*({dest_user}[^\s;@]+?)(@({dest_domain}[^\s;]+?))?[\s;]*\w+\s\w+(:|=)""",
  """Used(:|=)[^\"]+?Account Domain(:|=)\s*(\\r|\\n|\\t)*((?i)(NULL)|({dest_domain}[^\s;]+?))(\\r|\\n|\\t)*[\s;]*(Logon GUID|Callout Information)(:|=)""",
  """Used(:|=)[^\"]+?Logon GUID(:|=)(\\[rnt]|\s)*\{({account_login_guid}[^\s;]+?)\}[\s;]*(\\[rnt]|\s)*\w+\s\w+(:|=)""",
  """Target Server Name(:|=)(\\[rnt]|\s)*({dest_host}[\w\-\.]+)""",
  """Additional Information(:|=)\s*(\\r|\\t|\\n)*({dest_service_name}[^=:\s;\\]+)"""
  """Process ID(:|=)\s*(\\t)*({process_id}[^=:\s;\\]+)[\s;\\]*""",
  """Process Name(:|=)\s*(\\r|\\t|\\n)*(-|({process_path}({process_dir}\w:([^:=]+)?)[\\\/])?\s*(|({process_name}[^\\\/;\s]+\.\w+)))(;|\s|\\[rnt]|\s)+|Process Name"""
  """Network Address(:|=)(\\[rnt]|\s)*(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
  """Used(:|=);?\s*.+?Account Name(:|=)\s*(\\t|\\r|\\n)*\s*({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)[\s;]*(\\t|\\r|\\n)*\s*"""
  """Used(:|=);?\s*.+?Account Name(:|=)\s*(({dest_domain}[^\/"]+?)[\/]+?)?({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)[\s;]*(\\t|\\r|\\n)*\s*Account Domain"""
]
DupFields = [
"dest_user->account",
"dest_domain->account_domain"
]
ParserVersion = "v1.0.0"


}
```