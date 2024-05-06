#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-user-unlock-success-4767-3"
Conditions = [
""""data.id":"4767""""
""""type":"wazuh-alerts""""
""""decoder.parent":"windows""""
]
ExtractionType = json
ParserVersion = "v1.0.0"

json-windows-events-1.Fields}[
    """({event_name}A user account was disabled)""",
    """"hostname"+:"+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({host}[^"]+))""",
  
}
```