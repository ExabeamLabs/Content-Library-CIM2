#### Parser Content
```Java
{
Name = mariadb-m-csv-database-login-fail-failedconnect
Vendor = "MariaDB"
Product = "MariaDB"
TimeFormat = "yyyyMMdd HH:mm:ss"
Conditions = [
  """ mariadb """
  """,FAILED_CONNECT,"""
]
Fields = [
  """ mariadb ({time}\d{1,8} \d\d:\d\d:\d\d),"""
  """\:\d{2}\,(|({host}[^\,]+))\,(|({user}[^\,]+))\,(|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),(|({connection_id}\d+))\,(|({query_id}\d+))\,(|({db_operation}\w+))\,(|({db_name}[^\,]+))\,(|({object}[^\,]+)),"""
]
ParserVersion = "v1.0.0"


}
```