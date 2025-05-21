#### Parser Content
```Java
{
Name = "microsoft-evterminalservicesgateway-kv-endpoint-login-success-sessionlogon"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - TerminalServices-Gateway"
  TimeFormat = ["EEE MMM dd HH:mm:ss yyyy", "MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = ["""Microsoft-Windows-TerminalServices-LocalSessionManager""", """Remote Desktop Services: Session logon succeeded"""]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?""",
    """({time}\w+\s+\w+\s+\d+:\d+:\d+ \d+)""",
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-\.]+)\sMSWinEventLog""",
    """({event_name}Remote Desktop Services: Session logon succeeded)""",
    """\sUser:\s*(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\sSession ID:\s*({session_id}\d+)""",
    """\sSource Network Address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    ]


}
```