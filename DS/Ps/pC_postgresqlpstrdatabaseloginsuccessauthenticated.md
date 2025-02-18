#### Parser Content
```Java
{
Name = postgresql-p-str-database-login-success-authenticated
 Conditions = [""":LOG:""", """ connection authenticated:""", """identity=""", """ method=""" ]
 Fields = ${postgresqlParser-Template.postgresql-parser-str.Fields}[
   """identity=\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
   """method=({method}[^\s]+)"""
 ]


}
```