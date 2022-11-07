#### Parser Content
```Java
{
Name = postgresql-p-csv-database-login-success-authentication
  Vendor = PostgreSQL
  Product = PostgreSQL
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """connection authorized:""", """user=""", """database=""", """authentication""", """,LOG,""" ]
  Fields = [
    """({time}\d{4}-\d{2}-\d{2}\s(\d{2}:){2}\d{2}\.\d{3,})\sUTC""",
    """({action}connection authorized):\suser=({db_user}[^=]+?)\sdatabase=({db_name}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"
  DupFields = ["db_user -> user"]


}
```