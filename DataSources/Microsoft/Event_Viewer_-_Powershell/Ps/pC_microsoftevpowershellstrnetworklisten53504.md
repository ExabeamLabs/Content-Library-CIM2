#### Parser Content
```Java
{
Name = microsoft-evpowershell-str-network-listen-53504
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = Event Viewer - Powershell
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [ """53504""", """Microsoft-Windows-PowerShell""", """Windows PowerShell has started an IPC listening thread""" ]
  Fields = [
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\sMSWinEventLog""",
    """({event_code}53504)""",
    """Microsoft-Windows-PowerShell\s+(NETWORK SERVICE|({user}.+?))\s+User""",
    """({event_name}Windows PowerShell has started an IPC listening thread)""",
    """process:\s*({process_id}\d+)""",
    """({process_name}PowerShell)""",
  ]


}
```