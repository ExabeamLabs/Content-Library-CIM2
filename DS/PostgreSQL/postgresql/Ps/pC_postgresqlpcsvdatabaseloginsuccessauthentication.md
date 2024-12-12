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
    """({additional_info}({action}connection authorized):\s*(\[[^\]]+\]:|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)?\s*user=({db_user}[^=]+?)\sdatabase=({db_name}[^"\s=]+)("|\s)(application_name=({app}[^\s]+)\s)?[^"]*)""""
  ]
  ParserVersion = "v1.0.0"
  DupFields = ["db_user -> user"]


}
```