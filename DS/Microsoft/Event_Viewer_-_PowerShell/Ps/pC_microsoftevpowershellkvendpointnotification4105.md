#### Parser Content
```Java
{
Name = microsoft-evpowershell-kv-endpoint-notification-4105
  ParserVersion = "v1.0.0"
  Product = Event Viewer - PowerShell
  Conditions = [ """eventid="4105"""", """Microsoft-Windows-TerminalServices-Licensing""" ]
  Fields = ${WindowsParsersTemplates.windows-events-2.Fields}[
    """({event_name}The Remote Desktop license server cannot update the license attributes.+?)\s*$""",
# event_source_name is removed
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