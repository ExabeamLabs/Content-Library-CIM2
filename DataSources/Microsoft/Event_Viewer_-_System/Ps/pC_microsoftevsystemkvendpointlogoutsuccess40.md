#### Parser Content
```Java
{
Name = microsoft-evsystem-kv-endpoint-logout-success-40
  ParserVersion = "v1.0.0"
  Product = Event Viewer - System
  Conditions = [ """eventid="40"""", """Microsoft-Windows-TerminalServices-LocalSessionManager""" ]
  Fields = ${WindowsParsersTemplates.windows-events-2.Fields}[
    """({event_name}Session 26 has been disconnected, reason code 11)""",
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