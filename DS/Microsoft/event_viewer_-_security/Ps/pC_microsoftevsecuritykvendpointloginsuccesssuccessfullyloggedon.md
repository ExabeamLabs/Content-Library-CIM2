#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-successfullyloggedon"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "MM/dd/yyy HH:mm:ss"
Conditions = [
  """An account was successfully logged on"""
  """Account Name"""
  """Computer"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)""",
  """ComputerHOST644=({host}[\w\-.]+)\s\w+=""",
  """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d)""",
  """({operation}({event_name}An account was successfully logged on))""",
  """Computer_name:({host}[^\s]+)""",
  """ComputerName =({host}({dest_host}[\w\-\.]+))([^\s]*\s|;)""",
  """({event_code}4624)""",
  """Logon Type(:|=)\s*(\\t|\\r|\\n)*({login_type}\d+)""",
  """New Logon(:|=)[\s;]*(\\t|\\r|\\n)*Security ID(:|=)[^\}:]*?Account Name(:|=)\s*(\\t|\\r|\\n)*(-|SYSTEM|(({user_upn}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))[\s;]*(\\t|\\r|\\n)*Account Domain(:|=)""",
  """New Logon(:|=)[^\}]*?Account Domain(:|=)\s*(\\t|\\r|\\n)*(-|({dest_domain}({domain}[^\s]+?)))[\s;]*(\\t|\\r|\\n)*Logon ID(:|=)""",
  """Process Name(:|=)\s*(\\t|\\r|\\n)*(?:-|({process_path}({process_dir}[^\}]*?)(\\+({process_name}[^\\]+?))?))\s*(\\t|\\r|\\n)*(Network Information:|Additional Information:)""",
  """Workstation Name(:|=)\s*(\\t|\\r|\\n)*(-|[A-Fa-f:\d.]+|(?:\\+)?({src_host_windows}({src_host}[\w.\-]+\$?)))[\s;]*(\\t|\\r|\\n)*Source Network Address(:|=)""",
  """Source Network Address(:|=)\s*(\\t|\\r|\\n)*(?:-|({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f\d]+:[A-Fa-f\d:]+)))[\s;]*(\\t|\\r|\\n)*Source Port(:|=)""",
  """Logon Process(:|=)\s*(\\t|\\r|\\n)*({auth_process}[^\s;]+?)[\s;]*(\\t|\\r|\\n)*Authentication Package(:|=)\s*(\\t|\\r|\\n)*({auth_package}[^\s;\\]+)""",
  """Logon ID(:|=)\s*(\\t|\\r|\\n)*({login_id}[^\s;]+?)[\s;]*(\\t|\\r|\\n)*(Linked Logon|Logon GUID)""",
  """New Logon(:|=)[\s;]*(\\t|\\r|\\n)*Security ID(:|=)\s*(\\t|\\r|\\n)*(NT AUTHORITY\\+SYSTEM|({dest_user_sid}({user_sid}[^;:=]+?)))[\s;]*(\\t|\\r|\\n)*Account Name(:|=)""",
  """Key Length(:|=)\s*(\\t|\\r|\\n)*({key_length}\d+)""",
  """Subject(:|=)[\s;]*(\\t|\\r|\\n)*Security ID(:|=)\s*(\\t|\\r|\\n)*({subject_sid}[^;:=]+?)[\s+;]*(\\t|\\r|\\n)*Account Name(:|=)""",
  """Linked Logon ID:\s*(\\t|\\r|\\n)*({dest_login_id}[^\s\\]+)""",
  """Computer(\w+)?[\"\s]*(:|=)\s*\"?({dest_host}({host}[\w\-.]+?))(\"|\s|;)""",
]
ParserVersion = "v1.0.0"


}
```