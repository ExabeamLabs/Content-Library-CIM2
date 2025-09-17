#### Parser Content
```Java
{
Name = postgresql-p-str-database-activity-fatal
 Conditions = ["""FATAL:""", """postgres"""]
 Fields = ${postgresqlParser-Template.postgresql-parser-str-1.Fields}[
   """\WFATAL:\s*({additional_info}.+$)"""
  ]


}
```