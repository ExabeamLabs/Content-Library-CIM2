#### Parser Content
```Java
{
Name = microsoft-evpowershell-str-network-listen-53504
  Vendor = Microsoft
  ParserVersion = "v1.0.0"
  Product = Event Viewer - PowerShell
  TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """53504""", """Microsoft-Windows-PowerShell""", """Windows PowerShell has started an IPC listening thread""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?""",
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s({host}[^\s]+)\sMSWinEventLog""",
    """({event_code}53504)""",
    """Microsoft-Windows-PowerShell\s+(NETWORK SERVICE|({user}[\w\.\-]{1,40}\$?))\s+User""",
    """({event_name}Windows PowerShell has started an IPC listening thread)""",
    """process:\s*({process_id}\d+)""",
    """({process_name}PowerShell)""",
  ]


}
```