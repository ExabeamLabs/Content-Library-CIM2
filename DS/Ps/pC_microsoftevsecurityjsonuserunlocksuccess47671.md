#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-unlock-success-4767-1"
Conditions = [
""""event_id":4767"""
"""Microsoft-Windows-Security-Auditing"""
"""A user account was unlocked"""
]
ParserVersion = "v1.0.0"

json-windows-events-1.Fields}[
    """({event_name}A user account was disabled)""",
    """"hostname"+:"+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({dest_host}[^"]+))""",
  
}
```