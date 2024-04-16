#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-peripheral-storage-insert-success-6422"
Conditions = [ """Microsoft-Windows-Security-Auditing""" ,"""<EventID>6422</EventID>"""]
ParserVersion = "v1.0.0"

json-windows-events-1.Fields}[
    """({event_name}A user account was disabled)""",
    """"hostname"+:"+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({dest_host}[^"]+))""",
  
}
```