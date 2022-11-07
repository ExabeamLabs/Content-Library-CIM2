#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-user-privilege-assign-success-4672-2
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  Conditions = [ """subject.logon_id""", """EventID""", """4672""" ]
  Fields = ${WindowsParsersTemplates.windows-events-2.Fields}[
       """privileges":\[({privileges}[^\]]+)""",
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