#### Parser Content
```Java
{
Name = "microsoft-evpowershell-str-endpoint-notification-40961"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - PowerShell"
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """40961""", """Microsoft-Windows-PowerShell""", """PowerShell console is starting up""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?""",
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\sMSWinEventLog""",
    """({event_code}40961)""",
    """Microsoft-Windows-PowerShell\s+(NETWORK SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+User""",
    """({event_name}PowerShell console is starting up)""",
    """({process_name}PowerShell)""",
  ]


}
```