#### Parser Content
```Java
{
Name = microsoft-windows-kv-scheduled-task-trigger-success-119
  ParserVersion = "v1.0.0"
  Conditions = [ """eventid="119"""", """Microsoft-Windows-TaskScheduler""" ]
  Fields = ${WindowsParsersTemplates.windows-events-2.Fields}[
    """({event_name}Task Scheduler launched)""",
    """to user\s*(?:[^\\]+\\+)?(SYSTEM|({user}[^"]+))""",
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