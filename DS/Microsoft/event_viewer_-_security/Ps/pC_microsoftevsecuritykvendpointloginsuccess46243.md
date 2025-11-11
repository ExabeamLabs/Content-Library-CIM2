#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-endpoint-login-success-4624-3"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss", "epoch", "epoch_sec", "MM/dd/yyyy hh:mm:ss a", "MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Conditions = [
    """An account was successfully logged on"""
    """Account Name"""
    """Microsoft-Windows-Security-Auditing"""
  ]
  Fields = [
    """({time}\w{3}\s\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s\d{4})\s+4624\s+Microsoft-Windows-Security-Auditing"""
    """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(?i)(AM|PM))"""
    """({event_name}An account was successfully logged on)"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """<TimeCreated SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)"""
    """"Computer(Name)?":"({host}({dest_host}[\w\-\.]+))"""
    """Computer(Name)?="?({host}({dest_host}[\w\-\.]+))"""
    """Audit\s*({host}[\w\-.]+)\s*Logon"""
    """({event_code}4624)"""
    """Logon Type(:|=)\s*(\\[nrt])*({login_type}\d+)"""
    """\sAccount Name:\s*(\\[ntr])*(-|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))(\s|(\\[ntr])*)\s+Account Domain:"""
    """New Logon:[^"]*?Account Name(:|=)\s*(\\[nrt])*(-|SYSTEM|(({user_upn}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+(\.[^\]\s"\\,\|]+)?)|({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))))\s*"""
    """New Logon:[^"]*?Account Domain(:|=)(\\[nrt]|\s)*(-|NT AUTHORITY|({domain}[^\s\\]+))(\\[nrt]|\s)*"""
    """Process Name(:|=)\s*(\\[nrt])*(?:-|({process_path}({process_dir}[^=]*?)(\\+({process_name}[^\\]+?))?))(\s+|(\\[nrt])*)Network Information:"""
    """Workstation Name(:|=)\s*(\\[nrt])*(-|[A-Fa-f:\d.]+|(::ffff:)?({src_host}[\w\-.]+))([\s;]*|(\\[rnt])*)Source Network Address(:|=)"""
    """Source Network Address(:|=)\s*(\\[nrt])*(?:-|(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)([\s;]*|(\\[nrt])*)Source Port(:|=)"""
    """Logon Process(:|=)\s*(\\[nrt])*({auth_process}[^\s;\\]+)([\s;]*|(\\[nrt])*)Authentication Package(:|=)\s*(\\[nrt])*({auth_package}[^\s;\\]+)(\\[nrt])*"""
    """New Logon:[^"]*?Logon ID(:|=)(\\[nrt]|\s)*({login_id}[^\s\\;]+)(\\[nrt]|\s)*"""
    """Linked Logon ID(:|=)\s*(\\[nrt])*({dest_login_id}[^\s\\;]+)\s*"""
    """New Logon(:|=)([\s;]*|(\\[nrt])*)Security ID(:|=)\s*(\\[nrt])*(NT AUTHORITY\\SYSTEM|({user_sid}[^;:=]+?))([\s;]*|(\\[nrt])*)Account Name(:|=)"""
    """:\d+:\d+\s+(\d\d\d\d|((?i)AM|PM)|(::ffff:)?(({dest_ip}[a-fA-F0-9.:]+)|({dest_host}[\w\-.]+)))\s"""
    """:\d+\.\d+(\+|-)\d+:\d+\s+(::ffff:)?(({dest_ip}[a-fA-F0-9.:]+)|({dest_host}[\w\-.]+))\s"""
    """Key Length(:|=)\s*(\\[nrt])*({key_length}\d+)"""
    """Subject(:|=)([\s;]*|(\\[nrt])*)Security ID(:|=)\s*(\\[nrt])*({subject_sid}S-[^=:;]+?)(\s+|;|(\\[nrt])*)Account Name(:|=)"""
    """Source Port(:|=)\s*(\\[ntr])*({src_port}\d+)\s*"""
    """"host":"({host}[^",]+)""""
    """TimeGenerated=({time}\d{10})"""
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)""""
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """"TimeCreated":".*?({time}\d{1,13}).*?","""
    """Process ID:\s*(\\[nrt])*({process_id}[^\s\\]+)(\s*|(\\[nrt])*)"""
    """TargetLinkedLogonId="({dest_login_id}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```