#### Parser Content
```Java
{
Name = "mysql-m-csv-database-query-success-write"
Vendor = "Mysql"
Product = "Mysql"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""mysql-server_auditing:"""
""",WRITE,"""
]
Fields = [
"""({host}[\w\.-]+)\s+mysql-server_auditing:"""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\S+\s+\S+\s+mysql-server_auditing:"""
"""({app}mysql)"""
"""mysql-server_auditing:\s*({db_name}[^,]+)\s*,"""
"""mysql-server_auditing:\s*([^,]*,)\s*({user}[^,]+)\s*,"""
"""mysql-server_auditing:\s*([^,]*,){2}\s*({src_host}[^,]+)\s*,"""
"""({db_operation}WRITE)"""
""",WRITE,\s*({db_name}[^,]+)\s*,"""
""",WRITE,[^,]+,\s*({table_name}[^,]+)\s*"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```