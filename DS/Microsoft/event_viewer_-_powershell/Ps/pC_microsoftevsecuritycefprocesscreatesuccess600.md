#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-process-create-success-600
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """CEF: """, """|Microsoft|PowerShell|""", """|PowerShell:600|""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\sahost=({host}[^\s]+)\s""",
    """\sad.ProcessID=({process_id}[^\s]+)\s""",
    """\sdeviceSeverity=({alert_severity}[^\s]+)\s""",
    """\srequestClientApplication=({parent_process_path}.+?)\scs2=""",
    """\smsg=({additional_info}.+?)\sart=""",
  ]
  ParserVersion = "v1.0.0"


}
```