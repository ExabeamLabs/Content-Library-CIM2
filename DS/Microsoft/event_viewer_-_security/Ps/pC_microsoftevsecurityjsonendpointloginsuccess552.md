#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-login-success-552
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = ["Logon attempt using explicit credentials", "Target Logon GUID:"]
  Fields = [
    """({event_name}Logon attempt using explicit credentials)""",
    """timestamp:({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
    """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
    """(?i)(((audit|success)( |_)(success|audit))|information)\s*(\s|\t|,|#\d+|<[^>]+>)\s*({host}[\w\-.]+?)\s*(\s|\t|,|#\d+|<[^>]+>)\s*""",
    """({event_code}552)""",
    """({host}[\w\-.]+)\/Security \(552\)""",
    """<Computer>({host}[\w\-.]+)</Computer>""",
    """Computer(\w+)?["\s]*(:|=)\s*"?({host}[\w\-.]+?)("|\s)""",
    """ComputerName =({host}[\w.\-]+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w\-\.]+)""",
    """User Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Domain:""",
    """Domain:\s*({domain}[\w\-\.]+(?:[\s\.\-\w])*?)\s*Logon ID:""",
    """Logon ID:\s*\(\w+(\,|\s)({login_id}\w+)\)\s*Logon GUID:""",
    """Logon GUID:\s*(?:-|\{({user_login_guid}[^}]+)\})""",
    """Target User Name:\s*({dest_user}[\w\-\.]+(?:\s\w+)?\$?)\s*Target Domain:""",
    """Target Domain:\s*({dest_domain}[\w\-\.]+(?:[\s\.\-\w])*?)\s*Target Logon GUID:""",
    """Target Logon GUID:\s*(?:-|\{({account_login_guid}[^}]+)\})\s*Target Server Name:""",
    """Target Server Name:\s*(\\+[srnt])*({dest_host}[\w\-.]+?)(\\+[srnt])*\s*Target Server Info:""",
    """Target Server Info:\s*({dest_service_name}.+?)\s*Caller Process ID:""",
    """Source Network Address:\s+(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  ]


}
```