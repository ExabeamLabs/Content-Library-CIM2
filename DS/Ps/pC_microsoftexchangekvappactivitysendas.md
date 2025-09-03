#### Parser Content
```Java
{
Name = "microsoft-exchange-kv-app-activity-sendas"
Conditions = [ """Office365""", """ COMMAND=SendAs """, """USERKEY=""", """ORGANIZATIONNAME=""", """SENDASUSER=""" ]
DupFields = [
  "email_subject->object"
  "email_attachments->additional_info"
]
ParserVersion = "v1.0.0"


}
```