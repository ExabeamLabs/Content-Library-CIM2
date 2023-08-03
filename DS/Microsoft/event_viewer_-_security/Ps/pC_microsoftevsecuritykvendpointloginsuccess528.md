#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-success-528
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ "Logon Type:", "Successful Logon:" ]
  Fields = [
    """({event_name}Successful Logon)""",
    """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
    """\s(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)\s+528\s+Security\s""",
    """(?i)(((audit|success)( |_)(success|audit))|information)\s*,?\s*({host}[\w\-.]+)""",
    """"dhn":"({host}[^-"]+)""",
    """Computer(\w+)?["\s]*(:|=)\s*"?({host}.+?)("|\s)""",
    """({event_code}528)""",
    """User Name\s*:\s*({user}[\w\.\-]{1,40}\$?)\s+Domain:\s+({domain}[^\s]+)""",
    """Source Network Address\s*:\s*(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+Source Port:""",
    """Workstation Name\s*:\s*({src_host_windows}[^\s]+)\s*""",
    """Workstation Name\s*:\s*({src_host}[^\s]+).*?Source Network Address:\s*-\s+""",
    """Logon Process\s*:\s*({auth_process}.+?)\s+Authentication Package\s*:\s*({auth_package}[^\s]+)""",
    """Logon ID\s*:\s*[^,\s]+[,\s]({login_id}[^\)]+)\)\s+Logon Type\s*:\s*({login_type}\d+)""",
    """Security,({event_id}\d+)""",
    """\sSecurity.+?({event_id}\d+)\s+(Mon|Tue|Wed|Thu|Fri|Sat|Sun)\s""",
    """Sid=({user_sid}[^\s]+)\s+SidType"""
  ]
  DupFields = [ "host->dest_host" ]


}
```