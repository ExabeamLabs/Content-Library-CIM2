#### Parser Content
```Java
{
Name = pan-ngfw-cef-app-activity-success-hipreport
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|Palo Alto Networks|PAN-OS|""", """|GLOBALPROTECT|""", """PanOSEventID=gateway-hip-report""" ]
  DupFields = [ "event_name->operation" ]


}
```