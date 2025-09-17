#### Parser Content
```Java
{
Name = postgresql-p-str-database-activity-detail
 Conditions = ["""DETAIL:""", """postgres"""]
 Fields = ${postgresqlParser-Template.postgresql-parser-str-1.Fields}[
   """\WDETAIL:\s*({additional_info}.+$)"""
 ]


}
```