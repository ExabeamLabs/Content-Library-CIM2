#### Parser Content
```Java
{
Name = pan-ngfw-cef-app-activity-success-globalprotect-1
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|Palo Alto Networks|""", """|GLOBALPROTECT|""", """=gateway-getconfig""" ]
  DupFields = [ "event_name->operation" ]


}
```