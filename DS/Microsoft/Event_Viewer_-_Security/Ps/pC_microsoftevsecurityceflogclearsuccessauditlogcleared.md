#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-log-clear-success-auditlogcleared
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch"
  Conditions = ["""CEF:""", """Microsoft|Microsoft Windows|""", """Microsoft-Windows-Eventlog:1102""", """The audit log was cleared.|""" ]
  Fields = [
    """({event_code}1102)""",
    """\srt=({time}\d{10,13})""",
    """({event_name}The audit log was cleared)""",
    """\sdhost=({src_host}[\w\.\-]+)""",
    """\sdst=({dest_ip}[A-Fa-f.:\d]+)""",
    """\Wdntdom=({domain}[^=]+?)\s[\w\-\.]+=""",
    """\Wduser=({user}[^=]+?)\s*[\w\.\-]+=""",
    """dvchost=({host}[\w\.\-]+)""",
    """cs2=({category}[^=]+?)\s*[\w\-\.]+="""
  ]
  ParserVersion = "v1.0.0"


}
```