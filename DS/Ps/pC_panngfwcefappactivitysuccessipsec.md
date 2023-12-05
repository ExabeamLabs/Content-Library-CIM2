#### Parser Content
```Java
{
Name = pan-ngfw-cef-app-activity-success-ipsec
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|Palo Alto Networks|PAN-OS|""", """|GLOBALPROTECT|""", """PanOSEventID=gateway-setup-ipsec""" ]
  DupFields = [ "event_name->operation" ]


}
```