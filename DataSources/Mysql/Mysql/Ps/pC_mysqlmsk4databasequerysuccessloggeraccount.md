#### Parser Content
```Java
{
Name = mysql-m-sk4-database-query-success-loggeraccount
  Vendor = Mysql
  Product = Mysql
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"message":""", """"ttam_category":"database/mysql"""", """"ttam_service":"database"""", """logger.account""" ]
  Fields = [
    """timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
    """ttam_reporter":"({host}[^"]+)"""",
    """message":"\s*({db_query}({db_operation}\w+)[^"]*?)\s*"(,"\w+":|\})""",
    """message":"([^,]+,){5}({error_code}\d+),\\?"\s*({db_query}({db_operation}\w+)[^\}]*?)\s*"(,"\w+":|\})""",
    """({app}mysql)"""
  ]
  DupFields = [ "host->dest_host" ]


}
```