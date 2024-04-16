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
  """({event_name}An account was successfully logged on)""",
  """Computer_name:({host}[^\s]+)""",
  """ComputerName =({host}({dest_host}[\w\-\.]+))([^\s]*\s|;)""",
  """({event_code}4624)""",
  """Logon Type(:|=)\s*({login_type}\d+)""",
  """New Logon(:|=)[^\}]*?Account Name(:|=)\s*(-|SYSTEM|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)))[\s;]*Account Domain(:|=)""",
  """New Logon(:|=)[^\}]*?Account Domain(:|=)\s*(-|({domain}[^\s]+?))[\s;]*Logon ID(:|=)""",
  """Process Name(:|=)\s*(?:-|({process_path}({process_dir}[^\}]*?)(\\+({process_name}[^\\]+?))?))\s+Network Information:""",
  """Workstation Name(:|=)\s*(-|[A-Fa-f:\d.]+|({src_host_windows}[^\s;]+))[\s;]*Source Network Address(:|=)""",
  """Source Network Address(:|=)\s*(?:-|({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f\d]+:[A-Fa-f\d:]+)))[\s;]*Source Port(:|=)""",
  """Logon Process(:|=)\s*({auth_process}[^\s;]+)[\s;]*Authentication Package(:|=)\s*({auth_package}[^\s;]+)""",
  """Logon ID(:|=)\s*({login_id}[^\s;]+)[\s;]*(Linked Logon|Logon GUID)""",
  """New Logon(:|=)[\s;]*Security ID(:|=)\s*(NT AUTHORITY\\+SYSTEM|({user_sid}[^;:=]+?))(\s+|;)Account Name(:|=)""",
  """Key Length(:|=)\s*({key_length}\d+)""",
  """Subject(:|=)[\s;]*Security ID(:|=)\s*({subject_sid}[^;:=]+?)(\s+|;)Account Name(:|=)"""
]
DupFields = [ "src_host_windows->src_host" ]
ParserVersion = "v1.0.0"


}
```