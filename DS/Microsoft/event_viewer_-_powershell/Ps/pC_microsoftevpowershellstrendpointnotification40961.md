#### Parser Content
```Java
{
Name = "microsoft-evpowershell-str-endpoint-notification-40961"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - PowerShell"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """40961""", """Microsoft-Windows-PowerShell""", """PowerShell console is starting up""" ]
  Fields = [
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\sMSWinEventLog""",
    """({event_code}40961)""",
    """Microsoft-Windows-PowerShell\s+(NETWORK SERVICE|({user}.+?))\s+User""",
    """({event_name}PowerShell console is starting up)""",
    """({process_name}PowerShell)""",
  ]


}
```