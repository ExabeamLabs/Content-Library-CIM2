#### Parser Content
```Java
{
Name = mariadb-m-csv-database-modify-success-write
Vendor = MariaDB
Product = MariaDB
TimeFormat = "yyyyMMdd HH:mm:ss"
Conditions = [
  """MariaDB:"""
  """WRITE"""
]
Fields = [
  """MariaDB:\s({time}\d+\s\d\d:\d\d:\d\d)"""
  """\:\d{2}\,({host}[^\,]+)?\,({user}[^\,]+)?\,({src_ip}[^,]+)?,({connection_id}\d+)?\,({query_id}\d+)?\,({db_operation}\w+)?\,({db_name}[^\,]+)?\,({object}[^\,]+)?"""
]
ParserVersion = "v1.0.0"


}
```