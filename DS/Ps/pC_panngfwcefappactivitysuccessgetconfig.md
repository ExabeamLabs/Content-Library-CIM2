#### Parser Content
```Java
{
Name = pan-ngfw-cef-app-activity-success-getconfig
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|Palo Alto Networks|""", """|GLOBALPROTECT|""", """=portal-getconfig""" ]
  DupFields = [ "event_name->operation" ]


}
```