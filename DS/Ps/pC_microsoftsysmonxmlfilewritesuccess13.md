#### Parser Content
```Java
{
Name = "microsoft-sysmon-xml-file-write-success-13"
Conditions = [
  """<EventID>13</EventID>"""
  """<Provider Name"""
  """<Execution ProcessID="""
  """Microsoft-Windows-Sysmon"""
]
ParserVersion = "v1.0.0"

json-windows-events-1.Fields}[
    """({event_name}A user account was disabled)""",
    """"hostname"+:"+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({host}[^"]+))""",
  
}
```