#### Parser Content
```Java
{
Name = cisco-ucm-kv-app-login-success-userlogging
  ParserVersion = v1.0.0
  Product = cisco unified cm
  Conditions = [ """EventType =UserLogging""", """[ AuditDetails =""" ]
  DupFields = [ "additional_info->event_name" ]


}
```