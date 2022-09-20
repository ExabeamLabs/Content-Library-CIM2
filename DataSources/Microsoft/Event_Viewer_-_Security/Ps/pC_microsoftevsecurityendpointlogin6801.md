#### Parser Content
```Java
{
Name = microsoft-evsecurity-endpoint-login-680-1
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ "Logon attempt by:" ]
  Fields = [
    """({event_name}Logon attempt)""",
    """({time}\w{3}\s\d{2}\s\d{2}:\d{2}:\d{2}\s\d{4})""",
    """({event_code}680)""",
    """(?i)(((audit|success|failure)( |_)(success|audit|failure))|information)(\s+|\s*,\s*)({host}[\w\.\-]+)""",
    """Source Workstation:\s+(\\+)?({dest_host}[^\s.]+)[^\s]*.+Error Code:\s+({result_code}[^\s]+)""",
    """Logon (?:a|A)ccount:\s+({user}[^@]+?)(?:@({domain}[^\s]+))?\s+Source""",
    """(Information|Audit Success|Success Audit|Audit Failure|Failure Audit)\s+[^\s.]+\.({domain}[^\s.]+)""",
    """(?:Success|Audit)\s+\w+\s+[^\s.]+(\.({domain}[^\s.]+)[^\s]*)"""
  ]


}
```