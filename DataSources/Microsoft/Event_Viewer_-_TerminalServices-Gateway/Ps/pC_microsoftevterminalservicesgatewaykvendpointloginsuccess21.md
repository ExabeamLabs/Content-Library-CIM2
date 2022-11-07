#### Parser Content
```Java
{
Name = microsoft-evterminalservicesgateway-kv-endpoint-login-success-21
  ParserVersion = "v1.0.0"
  Product = Event Viewer - TerminalServices-Gateway
  Conditions = [ """eventid="21"""", """Microsoft-Windows-TerminalServices-LocalSessionManager""" ]
  Fields = ${WindowsParsersTemplates.windows-events-2.Fields}[
    """({event_name}Remote Desktop Services: Session logon succeeded)""",
    """\sUser:\s*(?:[^\\]+\\+)?(SYSTEM|({user}[^\s"]+))""",
    """\sSession ID:\s*({session_id}\d+)""",
    """\sSource Network Address:\s*({src_ip}\d+.\d+.\d+.\d+)""",
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