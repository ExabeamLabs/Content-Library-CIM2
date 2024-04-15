#### Parser Content
```Java
{
Name = "microsoft-evsecurity-sk4-endpoint-login-success-4624"
Conditions = [
""""EventId":4624"""
"""An account was successfully logged on"""
"""Microsoft-Windows-Security-Auditing"""
""""MachineName":"""
""""TimeCreated":"""
]
ParserVersion = "v1.0.0"

json-windows-events-1.Fields}[
    """({event_name}A user account was disabled)""",
    """"hostname"+:"+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({dest_host}[^"]+))""",
  
}
```