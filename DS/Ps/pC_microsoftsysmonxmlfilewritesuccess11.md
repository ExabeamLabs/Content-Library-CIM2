#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-file-write-success-11"
Conditions = [
  """<Provider Name"""
  """'Microsoft-Windows-Sysmon'"""
  """<EventID>11</EventID>"""
]
ParserVersion = "v1.0.0"

json-windows-events-1.Fields}[
    """({event_name}A user account was disabled)""",
    """"hostname"+:"+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({dest_host}[^"]+))""",
  
}
```