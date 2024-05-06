#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-user-enable-success-4722-1
Conditions = [
  """"event_id":4722"""
  """Microsoft-Windows-Security-Auditing"""
  """A user account was enabled"""
]
ExtractionType = json
ParserVersion = "v1.0.0"

json-windows-events-1.Fields}[
    """({event_name}A user account was disabled)""",
    """"hostname"+:"+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({host}[^"]+))""",
  
}
```