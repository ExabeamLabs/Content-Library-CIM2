#### Parser Content
```Java
{
Name = microsoft-evpowershell-str-endpoint-notification-40962
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = Event Viewer - PowerShell
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """40962""", """Microsoft-Windows-PowerShell""", """PowerShell console is ready for user input""" ]
  Fields = [
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\sMSWinEventLog""",
    """({event_code}40962)""",
    """Microsoft-Windows-PowerShell\s+(NETWORK SERVICE|({user}[\w\.\-]{1,40}\$?))\s+User""",
    """({event_name}PowerShell console is ready for user input)""",
    """({process_name}PowerShell)""",
  ]


}
```