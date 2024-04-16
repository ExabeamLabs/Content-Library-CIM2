#### Parser Content
```Java
{
Name = pan-ngfw-cef-app-activity-success-tunnellatency
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|Palo Alto Networks|""", """|GLOBALPROTECT|""", """=gateway-tunnel-latency""" ]
  DupFields = [ "event_name->operation" ]


}
```