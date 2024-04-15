#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-4624-3"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
    """An account was successfully logged on"""
    """Account Name"""
    """Microsoft-Windows-Security-Auditing"""
  ]
  Fields = [
    """({time}\w+\s\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s\d{4})\s+4624\s+Microsoft-Windows-Security-Auditing"""
    """({event_name}An account was successfully logged on)"""
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """Computer(Name)?="?({host}[^\s"]+)"""
    """Audit\s*({host}[^\s]+)\s*Logon"""
    """({event_code}4624)"""
    """Logon Type(:|=)\s*({login_type}\d+)"""
    """New Logon[^"]*?Account Name(:|=)\s*(-|SYSTEM|({user}[^\s]+))"""
    """New Logon[^"]*?Account Domain(:|=)\s*(-|NT AUTHORITY|({domain}[^\s]+))"""
    """Process Name(:|=)\s*(?:-|({process_path}({process_dir}[^=]*?)(\\+({process_name}[^\\]+?))?))\s+Network Information:"""
    """Workstation Name(:|=)\s*(-|[A-Fa-f:\d.]+|(::ffff:)?({src_host_windows}[^\s;]+))[\s;]*Source Network Address(:|=)"""
    """Source Network Address(:|=)\s*(?:-|(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)[\s;]*Source Port(:|=)"""
    """Logon Process(:|=)\s*({auth_process}[^\s;]+)[\s;]*Authentication Package(:|=)\s*({auth_package}[^\s;]+)"""
    """Logon ID(:|=)\s*({login_id}[^\s;]+)"""
    """New Logon(:|=)[\s;]*Security ID(:|=)\s*(NT AUTHORITY\\SYSTEM|({user_sid}[^;:=]+?))[\s;]*Account Name(:|=)"""
    """:\d+:\d+\s+(\d\d\d\d|((?i)AM|PM)|(::ffff:)?(({dest_ip}[a-fA-F0-9.:]+)|({dest_host}[\w\-.]+)))\s"""
    """:\d+\.\d+(\+|-)\d+:\d+\s+(::ffff:)?(({dest_ip}[a-fA-F0-9.:]+)|({dest_host}[\w\-.]+))\s"""
    """Key Length(:|=)\s*({key_length}\d+)"""
    """Subject(:|=)[\s;]*Security ID(:|=)\s*({subject_sid}[^;:=]+?)(\s+|;)Account Name(:|=)"""
    """Source Port(:|=)\s*({src_port}\d+)\s*"""
  ]
  ParserVersion = "v1.0.0"


}
```