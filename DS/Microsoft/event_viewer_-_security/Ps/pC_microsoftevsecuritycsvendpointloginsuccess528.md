#### Parser Content
```Java
{
Name = microsoft-evsecurity-csv-endpoint-login-success-528
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ "MSWinEventLog", " 528 Security", "Successful Logon:" ]
  Fields = [
    """({event_name}Successful Logon)""",
    """({time}\w{3}\s\d{2}\s\d{2}:\d{2}:\d{2}\s\d{4})""",
    """({event_code}528)""",
    """Information\s+({host}[\w.\-]+)\s+""",
    """(?:Success|Audit)\s+\w+\s+({host}[^\s]+)""",
    """Security\s+(rn=)?({event_id}\d+)""",
    """User Name:\s+({user}.+?)\s+Domain:\s+({domain}.+?)\s+Logon ID:\s+\([^,\s]+[,\s]({login_id}[^\)]+)\)\s+Logon Type:\s+({login_type}\d+)\s+Logon Process:""",
    """Logon Process:\s+({auth_process}.+?)\s+Authentication Package:\s+({auth_package}[^\s]+)""",
    """Source Network Address:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  DupFields = [ "host->dest_host" ]


}
```