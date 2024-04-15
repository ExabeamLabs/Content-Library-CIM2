#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-4624-2"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [
    """An account was successfully logged on"""
    """Account Name"""
    """dhn"""
  ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """({event_name}An account was successfully logged on)"""
    """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
    """"dhn":"({host}[^-"]+)"""
    """({event_code}4624)"""
    """Logon Type(:|=)\s*({login_type}\d+)"""
    """New Logon.*?Account Name(:|=)\s*(-|SYSTEM|({user}[^\s]+?))[\s;]*Account Domain(:|=)"""
    """New Logon.*?Account Domain(:|=)\s*(-|({domain}[^\s]+?))[\s;]*Logon ID(:|=)"""
    """Process Name(:|=)\s*(?:-|({process_path}({process_dir}.*?)(\\+({process_name}[^\\]+?))?))\s+Network Information:"""
    """Workstation Name(:|=)\s*(-|[A-Fa-f:\d.]+|({src_host_windows}[^\s;]+))[\s;]*Source Network Address(:|=)"""
    """Source Network Address(:|=)\s*(?:-|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)[\s;]*Source Port(:|=)"""
    """Logon Process(:|=)\s*({auth_process}[^\s;]+)[\s;]*Authentication Package(:|=)\s*({auth_package}[^\s;]+)"""
    """Logon ID(:|=)\s*({login_id}[^\s;]+)[\s;]*(Linked Logon|Logon GUID)"""
    """New Logon(:|=)[\s;]*Security ID(:|=)\s*({user_sid}[^\s;]+)(\s|;)"""
  ]
  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```