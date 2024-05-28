#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-4624-3"
  ExtractionType = json
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss", "epoch", "epoch_sec", "MM/dd/yyyy hh:mm:ss a", "MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
  Conditions = [
    """An account was successfully logged on"""
    """Account Name"""
    """Microsoft-Windows-Security-Auditing"""
  ]
  Fields = [
    """({time}\w+\s\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s\d{4})\s+4624\s+Microsoft-Windows-Security-Auditing"""
    """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
    """({event_name}An account was successfully logged on)"""
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)"""
    """"Computer(Name)?":"({host}({dest_host}[\w\-\.]+))"""
    """Computer(Name)?="?({host}({dest_host}[\w\-\.]+))"""
    """Audit\s*({host}[\w\-.]+)\s*Logon"""
    """({event_code}4624)"""
    """Logon Type(:|=)\s*({login_type}\d+)"""
    """New Logon:[^"]*?Account Name(:|=)\s*(-|SYSTEM|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)))\s*"""
    """New Logon:[^"]*?Account Domain(:|=)(\\[nrt]|\s)*(-|NT AUTHORITY|({domain}[^\s\\]+))(\\[nrt]|\s)*"""
    """Process Name(:|=)\s*(?:-|({process_path}({process_dir}[^=]*?)(\\+({process_name}[^\\]+?))?))\s+Network Information:"""
    """Workstation Name(:|=)\s*(-|[A-Fa-f:\d.]+|(::ffff:)?({src_host}[^\s;]+))[\s;]*Source Network Address(:|=)"""
    """Source Network Address(:|=)\s*(?:-|(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)[\s;]*Source Port(:|=)"""
    """Logon Process(:|=)\s*({auth_process}[^\s;]+)[\s;]*Authentication Package(:|=)\s*({auth_package}[^\s;]+)"""
    """New Logon:[^"]*?Logon ID(:|=)(\\[nrt]|\s)*({login_id}[^\s\\;]+)(\\[nrt]|\s)*"""
    """Linked Logon ID(:|=)\s*({dest_login_id}[^\s\\;]+)\s*"""
    """New Logon(:|=)[\s;]*Security ID(:|=)\s*(NT AUTHORITY\\SYSTEM|({user_sid}[^;:=]+?))[\s;]*Account Name(:|=)"""
    """:\d+:\d+\s+(\d\d\d\d|((?i)AM|PM)|(::ffff:)?(({dest_ip}[a-fA-F0-9.:]+)|({dest_host}[\w\-.]+)))\s"""
    """:\d+\.\d+(\+|-)\d+:\d+\s+(::ffff:)?(({dest_ip}[a-fA-F0-9.:]+)|({dest_host}[\w\-.]+))\s"""
    """Key Length(:|=)\s*({key_length}\d+)"""
    """Subject(:|=)[\s;]*Security ID(:|=)\s*({subject_sid}[^;:=]+?)(\s+|;)Account Name(:|=)"""
    """Source Port(:|=)\s*({src_port}\d+)\s*"""
    """\sAccount Name:\s*(-|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)))\s""",
    """"host":"({host}[^",]+)""""
    """TimeGenerated=({time}\d{10})"""
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """"TimeCreated":".*?({time}\d{1,13}).*?","""
    """\s*Process ID:\s*({process_id}[^\s]+)\s*"""
    """\s*TargetLinkedLogonId="+({dest_login_id}[^"]+)""""

    """exa_json_path=$.Message,exa_regex=Logon Type(:|=)\s*({login_type}\d+)"""
    """exa_json_path=$.Message,exa_regex=New Logon:[^"]*?Account Name(:|=)\s*(-|SYSTEM|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)))\s*"""
    """exa_json_path=$.Message,exa_regex=New Logon:[^"]*?Account Domain(:|=)(\\[nrt]|\s)*(-|NT AUTHORITY|({domain}[^\s\\]+))(\\[nrt]|\s)*"""
    """exa_json_path=$.Message,exa_regex=Process Name(:|=)\s*(?:-|({process_path}({process_dir}[^=]*?)(\\+({process_name}[^\\]+?))?))\s+Network Information:"""
    """exa_json_path=$.Message,exa_regex=Workstation Name(:|=)\s*(-|[A-Fa-f:\d.]+|(::ffff:)?({src_host}[^\s;]+))[\s;]*Source Network Address(:|=)"""
    """exa_json_path=$.Message,exa_regex=Source Network Address(:|=)\s*(?:-|(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)[\s;]*Source Port(:|=)"""
    """exa_json_path=$.Message,exa_regex=Logon Process(:|=)\s*({auth_process}[^\s;]+)[\s;]*Authentication Package(:|=)\s*({auth_package}[^\s;]+)"""
    """exa_regex=New Logon:[^"]*?Logon ID(:|=)(\\[nrt]|\s)*({login_id}[^\s\\;]+)(\\[nrt]|\s)*"""
    """exa_json_path=$.Message,exa_regex=New Logon(:|=)[\s;]*Security ID(:|=)\s*(NT AUTHORITY\\SYSTEM|({user_sid}[^;:=]+?))[\s;]*Account Name(:|=)"""
    """exa_json_path=$.Message,exa_regex=Key Length(:|=)\s*({key_length}\d+)"""
    """exa_json_path=$.Message,exa_regex=Subject(:|=)[\s;]*Security ID(:|=)\s*({subject_sid}[^;:=]+?)(\s+|;)Account Name(:|=)"""
    """exa_json_path=$.Message,exa_regex=Source Port(:|=)\s*({src_port}\d+)\s*"""
    """exa_json_path=$.Message,exa_regex=\sAccount Name:\s*(-|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)))\s""",
    """exa_regex=({event_name}An account was successfully logged on)"""
    """exa_json_path=$.Id,exa_field_name=event_code"""
    """exa_json_path=$.host,exa_field_name=host"""
    """exa_json_path=$.TimeGenerated,exa_field_name=time"""
    """exa_json_path=$.TimeCreated,exa_regex=[\\\/]*Date\(({time}\d{13})"""
  ]
  DupFields = ["user->account"]
  ParserVersion = "v1.0.0"


}
```