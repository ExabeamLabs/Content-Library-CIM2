#### Parser Content
```Java
{
Name = "microsoft-defenderep-kv-alert-trigger-success-1116"
Conditions = [
"""<EventID>1116</EventID>"""
"""<Channel>Microsoft-Windows-Windows Defender/Operational</Channel>"""
"""<Data Name ='Product Name'>Microsoft Defender Antivirus</Data>"""
"""<Data Name ='Detection Time'>"""
]
ParserVersion = "v1.0.0"

json-windows-events-1.Fields}[
    """({event_name}A user account was disabled)""",
    """"hostname"+:"+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({dest_host}[^"]+))""",
  
}
```