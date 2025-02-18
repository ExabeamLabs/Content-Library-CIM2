#### Parser Content
```Java
{
Name = postgresql-p-str-database-logout-success-disconnect
 Conditions = [""":LOG:""", """ disconnection:""", """ session time:""", """ database=""" ]
 Fields = ${postgresqlParser-Template.postgresql-parser-str.Fields}[
   """session time:\s*({session_duration}[^=]+?)\s*\w+="""
 ]


}
```