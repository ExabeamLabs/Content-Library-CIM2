#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-success-540
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ "Logon Type:", "Successful Network Logon:" ]
  Fields = [
    """TimeGenerated=({time}\d{10})"""
    """({event_name}Successful Network Logon)""",
    """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
    """\s(Mon|Tue|Wed|Thu|Fri|Sat|Sun) ({time}\w+ \d+ \d+:\d+:\d+ \d+)\s+540\s+Security""",
    """(?i)(((audit|success)( |_)(success|audit))|information)\s*,?\s*({host}[\w\-.]+)""",
    """({host}[^\/\s]+)\/Security\s+\(""",
    """Computer(\w+)?["\s]*(:|=)\s*"?({host}[\w\-.]+?)("|\s)""",
    """({event_code}540)""",
    """User Name\s*:\s*(-|<null>|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Domain\s*:\s*(-|({domain}[^\s]+))\s""",
    """Source Network Address\s*:\s*(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+Source Port:""",
    """Workstation Name\s*:\s*(-|({src_host_windows}[^\s]+))\s+Logon GUID:""",
    """Workstation Name\s*:\s*({src_host}[^\s]+)\s+Logon GUID:.*?Source Network Address:\s*-\s+""",
    """Logon Process\s*:\s*({auth_process}.+?)\s+Authentication Package\s*:\s*({auth_package}.+?)\s+Workstation Name:""",
    """Logon ID\s*:\s*[^,\s]+[,\s]({login_id}[^\)]+)\)\s+Logon Type\s*:\s*({login_type}\d+)""",
    """Security(\s+|,)(rn=)?({event_id}\d+)"""
  ]
  DupFields = [ "host->dest_host" ]


}
```