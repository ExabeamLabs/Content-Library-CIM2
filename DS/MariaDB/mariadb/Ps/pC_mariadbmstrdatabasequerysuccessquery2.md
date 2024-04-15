#### Parser Content
```Java
{
Name = "mariadb-m-str-database-query-success-query-2"
Vendor = "MariaDB"
Product = "MariaDB"
TimeFormat = "yyyyMMdd HH:mm:ss"
Conditions = [
"""MariaDB:"""
"""QUERY"""
]
Fields = [
"""MariaDB:\s({time}\d+\s\d\d:\d\d:\d\d)"""
"""\:\d{2}\,({host}[^\,]+)?\,({user}[^\,]+)?\,({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({connection_id}\d+)?\,({query_id}\d+)?\,({db_operation}\w+)?\,({db_name}[^\,]+)?\,({db_query}.+)?\,\d+"""
]
ParserVersion = "v1.0.0"


}
```