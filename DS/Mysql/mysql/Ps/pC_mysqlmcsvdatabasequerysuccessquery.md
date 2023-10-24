#### Parser Content
```Java
{
Name = mysql-m-csv-database-query-success-query
  ParserVersion = v1.0.0
  Vendor = Mysql
  Product = Mysql
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """mysql-server_auditing:""", """,QUERY,""" ]
  Fields = [
    """({host}[\w\.-]+)\s+mysql-server_auditing:""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\S+\s+\S+\s+mysql-server_auditing:""",
    """({app}mysql)""",
    """mysql-server_auditing:\s*({db_name}[^,]+)\s*,""",
    """mysql-server_auditing:\s*([^,]*,)\s*({user}[\w\.\-]{1,40}\$?)\s*,""",
    """mysql-server_auditing:\s*([^,]*,){2}\s*({src_host}[^,]+)\s*,""",
    """,QUERY,({db_schema}[^,]+),""",
    """,QUERY,[^,]*,'\s*({db_operation}\S+)""",
    """,QUERY,[^,]*,'\s*({db_query}.*?[^\\])\s*',({error_code}\d+)?\s*$"""
  ]
  DupFields = [ "host->dest_host" ]


}
```