#### Parser Content
```Java
{
Name = sap-s-cef-endpoint-login-fail-secude
  Product = SAP
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|SECUDE|C-Bus|""", """|BU1|Password check failed for user|""" ]
  DupFields = [ "additional_info->failure_reason" ]


}
```