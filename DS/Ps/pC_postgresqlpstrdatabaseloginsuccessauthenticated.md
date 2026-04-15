#### Parser Content
```Java
{
Name = postgresql-p-str-database-login-success-authenticated
 Conditions = ["""LOG:""", """ connection authenticated:""", """ method=""" ]
 Fields = ${postgresqlParser-Template.postgresql-parser-str.Fields}[
   """identity=\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
   """method=({auth_method}[^\s]+)"""
   """db=({db_name}[^,]+)"""
 ]


}
```