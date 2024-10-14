#### Parser Content
```Java
{
Name = microsoft-evpowershell-str-endpoint-notification-success-53504
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Event Viewer - PowerShell
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """eventid="53504"""", """Microsoft-Windows-PowerShell""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z\s*({host}[^\s]+)\s""",
    """eventid="+({event_code}\d+)""",
    """providername="+({provider_name}[^"]+)""",
    """userid="(?:[^\\]+\\+)?(SYSTEM|NETWORK SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """\stask="+({operation}[^"]+)""",
    """\Weventrecordid="+({event_id}\d+)"""",
  """({event_name}Windows PowerShell has started an IPC listening thread)""",
  ]
  DupFields = ["event_id->event_code"]


}
```