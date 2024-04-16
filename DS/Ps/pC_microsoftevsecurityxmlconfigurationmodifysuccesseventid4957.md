#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-configuration-modify-success-eventid4957"
  Conditions = [
    """<EventID>4957</EventID>"""
    """<EventRecordID>"""
  ]
  ParserVersion = "v1.0.0" 

json-windows-events-1.Fields}[
    """({event_name}A user account was disabled)""",
    """"hostname"+:"+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({dest_host}[^"]+))""",
  
}
```