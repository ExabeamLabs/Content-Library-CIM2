#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-privilege-use-success-wazuhalerts"
Conditions = [
""""data.id":"4673""""
"""wazuh-alerts"""
""""decoder.parent":"windows""""
]
ParserVersion = "v1.0.0"

json-windows-events-1.Fields}[
    """({event_name}A user account was disabled)""",
    """"hostname"+:"+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({host}[^"]+))""",
  
}
```