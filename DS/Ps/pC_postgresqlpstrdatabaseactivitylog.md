#### Parser Content
```Java
{
Name = postgresql-p-str-database-activity-log
 Conditions = ["""LOG:""", """postgres"""]
 Fields = ${postgresqlParser-Template.postgresql-parser-str-1.Fields}[
   """\WLOG:\s*({additional_info}.+$)"""
 ]


}
```