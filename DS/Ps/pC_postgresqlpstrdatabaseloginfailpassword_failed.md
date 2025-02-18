#### Parser Content
```Java
{
Name = postgresql-p-str-database-login-fail-password_failed
 Conditions = [""":FATAL:""", """password authentication failed for user""" ]
 Fields = ${postgresqlParser-Template.postgresql-parser-str.Fields}[
   """password authentication failed for user\s*(\\*")*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
   """({operation}password authentication failed)"""
 ]


}
```