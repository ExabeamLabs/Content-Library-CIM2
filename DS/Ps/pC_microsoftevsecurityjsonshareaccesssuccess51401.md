#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-share-access-success-5140-1"
Conditions = [
  """"event_id":5140"""
  """Microsoft-Windows-Security-Auditing"""
  """A network share object was accessed"""
]
ParserVersion = "v1.0.0"

json-windows-events-1.Fields}[
    """({event_name}A user account was disabled)""",
    """"hostname"+:"+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({dest_host}[^"]+))""",
  
}
```