#### Parser Content
```Java
{
Name = cisco-duo-sk4-app-activity-success-admincreate
  Conditions = [ """"action":""", """"admin_create"""", """object":""", """"username":""", """description":""" ]
  ParserVersion = "v1.0.0"
} 

${DuoParsersTemplates.duo-app-activity-2}{
  Name = cisco-duo-json-app-activity-success-adminactivate
  Conditions = [ """ duo: """, """|admin_activate_duo_push|""", """": """" ]
  ParserVersion = "v1.0.0"


}
```