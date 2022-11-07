#### Parser Content
```Java
{
Name = mariadb-m-str-database-logout-success-disconnect
  Vendor = MariaDB
  Product = MariaDB
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyyMMdd HH:mm:ss"
  Conditions = [ """ mariadb """,""",DISCONNECT,""" ]
  Fields = [
    """ mariadb ({time}\d{1,8} \d\d:\d\d:\d\d),""",
    """\:\d{2}\,(|({host}[^\,]+))\,(|({user}[^\,]+))\,(|({src_ip}[^,]+)),(|({connection_id}\d+))\,(|({query_id}\d+))\,(|({db_operation}\w+))\,(|({db_name}[^\,]+))\,(|({object}[^\,]+)),"""
  ]


}
```