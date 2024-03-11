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
    """\srt=({time}\d{13})""",
    """({event_name}The audit log was cleared)""",
    """\sdhost=({dest_host}[\w\.\-]+)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdntdom=({domain}[^=]+?)\s[\w\-\.]+=""",
    """\Wduser=({user}[^=]+?)\s*[\w\.\-]+=""",
    """dvchost=({host}[\w\.\-]+)""",
    """cs2=({category}[^=]+?)\s*[\w\-\.]+="""
  ]
  ParserVersion = "v1.0.0"


}
```