#### Parser Content
```Java
{
Name = postgresql-p-str-database-activity-context
 Conditions = ["""CONTEXT:""", """postgres"""]
 Fields = ${postgresqlParser-Template.postgresql-parser-str-1.Fields}[
   """\WCONTEXT:\s*({additional_info}.+$)"""
   """\WSQL statement\s*"({db_query}[^\"]+)""""
 ]


}
```