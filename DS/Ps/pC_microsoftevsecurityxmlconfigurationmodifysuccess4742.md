#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-configuration-modify-success-4742"
  Conditions = [
    """<EventID>4742</EventID>"""
    """<EventRecordID>"""
  ]
  ParserVersion = "v1.0.0"

json-windows-events-1.Fields}[
    """({event_name}A user account was disabled)""",
    """"hostname"+:"+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({dest_host}[^"]+))""",
  
}
```