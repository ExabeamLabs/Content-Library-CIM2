#### Parser Content
```Java
{
Name = postgresql-p-str-database-login-fail-password-doesnotmatch
 Conditions = ["""DETAIL:""",""" Password does not match for user""" ]
 Fields = ${postgresqlParser-Template.postgresql-parser-str-1.Fields}[
   """({failure_reason}Password does not match) for user\s*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
 ]


}
```