#### Parser Content
```Java
{
Name = mariadb-m-csv-database-login-success-connect
Vendor = MariaDB
Product = MariaDB
TimeFormat = "yyyyMMdd HH:mm:ss"
Conditions = [
  """MariaDB:"""
  """CONNECT"""
]
Fields = [
  """MariaDB:\s({time}\d+\s\d\d:\d\d:\d\d)"""
  """\:\d{2}\,({host}[^\,]+)?\,({user}[^\,]+)?\,({src_ip}[^,]+)?,({connection_id}\d+)?\,({query_id}\d+)?\,({db_operation}\w+)?\,({db_name}[^\,]+)?"""
]
ParserVersion = "v1.0.0"


}
```