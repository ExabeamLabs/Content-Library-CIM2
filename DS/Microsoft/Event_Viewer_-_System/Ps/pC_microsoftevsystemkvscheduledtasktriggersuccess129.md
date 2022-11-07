#### Parser Content
```Java
{
Name = microsoft-evsystem-kv-scheduled-task-trigger-success-129
  ParserVersion = "v1.0.0"
  Product = Event Viewer - System
  Conditions = [ """eventid="129"""", """Microsoft-Windows-TaskScheduler""" ]
  Fields = ${WindowsParsersTemplates.windows-events-2.Fields}[
    """\sprocess ID\s*({process_id}\d+)""",
    """({event_name}Task Scheduler launch task)""",
  ]

windows-events-2 = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z\s*({host}[^\s]+)\s""",
    """eventid="+({event_code}\d+)""",
    """providername="+({provider_name}[^"]+)""",
    """userid="(?:[^\\]+\\+)?(SYSTEM|NETWORK SERVICE|({user}[^"]+))""",
    """\stask="+({operation}[^"]+)""",
    """\Weventrecordid="+({event_id}\d+)"""",
  ]
  DupFields = ["event_id->event_code"
}
```