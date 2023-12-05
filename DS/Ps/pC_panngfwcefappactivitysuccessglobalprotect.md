#### Parser Content
```Java
{
Name = pan-ngfw-cef-app-activity-success-globalprotect
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|Palo Alto Networks|PAN-OS|""", """|GLOBALPROTECT|""", """PanOSEventID=gateway-hip-check""" ]
  DupFields = [ "event_name->operation" ]


}
```