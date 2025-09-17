#### Parser Content
```Java
{
Name = postgresql-p-str-database-login-fail-role-doesnt_exist
 Conditions = ["""DETAIL:""", """  Role""", """ does not exist""" ]
 Fields = ${postgresqlParser-Template.postgresql-parser-str.Fields}[
   """Role\s*(\\*"*)({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
   """({failure_reason}Role\s*.+?does not exist)"""
 ]


}
```