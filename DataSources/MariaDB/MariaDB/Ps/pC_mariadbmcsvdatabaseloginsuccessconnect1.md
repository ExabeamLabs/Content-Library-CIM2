#### Parser Content
```Java
{
Name = mariadb-m-csv-database-login-success-connect-1
Vendor = "MariaDB"
Product = "MariaDB"
TimeFormat = "yyyyMMdd HH:mm:ss"
Conditions = [
  """ mariadb """
  """,CONNECT,"""
]
Fields = [
  """ mariadb ({time}\d{1,8} \d\d:\d\d:\d\d),"""
  """\:\d{2}\,(|({host}[^\,]+))\,(|({user}[^\,]+))\,(|({src_ip}[^,]+)),(|({connection_id}\d+))\,(|({query_id}\d+))\,(|({db_operation}\w+))\,(|({db_name}[^\,]+))\,(|({object}[^\,]+)),"""
]
ParserVersion = "v1.0.0"


}
```