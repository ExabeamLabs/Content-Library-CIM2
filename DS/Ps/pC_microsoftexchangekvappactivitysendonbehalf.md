#### Parser Content
```Java
{
Name = "microsoft-exchange-kv-app-activity-sendonbehalf"
Conditions = [ """Office365""", """ COMMAND=SendOnBehalf """, """USERKEY=""", """ORGANIZATIONNAME=""", """SENDONBEHALFOFUSER=""" ]
DupFields = [
  "email_subject->object"
  "email_attachments->additional_info"
]
ParserVersion = "v1.0.0"


}
```