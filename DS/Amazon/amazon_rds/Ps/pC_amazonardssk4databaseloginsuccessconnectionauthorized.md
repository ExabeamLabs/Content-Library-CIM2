#### Parser Content
```Java
{
Name = amazon-ards-sk4-database-login-success-connectionauthorized
  ParserVersion = v1.0.0
  Vendor = Amazon
  Product = Amazon RDS
  TimeFormat = "yyyy-MM-dd HH:mm:ss z"
  Conditions = [ """connection authorized:""", """user=""", """database=""" ]
  Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d \S+?):""",
      """LOG:\s*({event_name}connection authorized)""",
      """protocol=({protocol}[^",]+?),""",
      """user=({db_user}[^\s]+?)\s""",
      """database=({db_name}[^\s]+?)\s""" 
  ]
  DupFields = [ "db_user->user" ]


}
```