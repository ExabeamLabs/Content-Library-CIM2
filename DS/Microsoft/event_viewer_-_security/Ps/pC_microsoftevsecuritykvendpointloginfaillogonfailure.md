#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-fail-logonfailure
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = ["""Logon Failure""", """Reason:""", """Caller User Name:"""]
  Fields = [
    """TimeGenerated=({time}\d{10})"""
    """({event_name}Logon Failure)""",
    """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
    """(?i)(((audit|failure)( |_)(audit|failure))|information)\s*(\s|\t|,|#\d+|<[^>]+>)\s*({host}[^=]+?)\s*(\s|\t|,|#\d+|<[^>]+>)\s*""",
    """\d\d:\d\d:\d\d \d\d\d\d\s*(\s|\t|,|#\d+|<[^>]+>)\s*({event_code}\d+)\s*(\s|\t|,|#\d+|<[^>]+>)\s*Security""",
    """({host}[^\s\/]+)\/Security \(({event_code}\d+)\)""",
    """<Computer>({dest_host}({host}[\w\-.]+))</Computer>""",
    """Computer(\w+)?["\s]*(:|=)\s*"?({dest_host}({host}[\w\-.]+?))("|\s)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """Event(ID)?Code=({event_code}\d+)""",
    """Caller User Name:\s*(-|({user}[\w\.\-]{1,40}\$?))\s*Caller Domain:""",
    """Caller Domain:\s*(-|({src_domain}.+?))\s*Caller Logon ID:""",
    """User Name:\s*(?=\w)(-|([^\/]+?\/)?({user}[\w\.\-]{1,40}\$?))\s*Domain.+?Logon Type""",
    """Domain:\s*(?=\w)({domain}.+?)\s*Logon Type""",
    """Logon Type:\s*({login_type}\d+)\s+Logon Process:\s+({auth_process}.*?)\s+Authentication Package:\s+({auth_package}.*?)\s+Workstation Name:""",
    """Workstation Name:\s*(-|({src_host_windows}[^\s]+))\s*Caller User Name:""",
    """Workstation Name:\s*({src_host}[^\s]+)\s*Caller User Name:.*?Source Network Address:\s*-\s+""",
    """Caller User Name:\s*(?:-|({src_user}.+?))\s*Caller Domain:""",
    """Caller Domain:\s*({src_domain}.+?)\s*Caller Logon ID:\s*\([^,]+,({login_id}[^\)]+)""",
    """Source Network Address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  DupFields = ["event_code->result_code"]


}
```