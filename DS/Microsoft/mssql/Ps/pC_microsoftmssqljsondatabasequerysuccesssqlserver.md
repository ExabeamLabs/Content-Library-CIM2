#### Parser Content
```Java
{
Name = "microsoft-mssql-json-database-query-success-sqlserver"
Vendor = "Microsoft"
Product = "MSSQL"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSSSSS"
Conditions = [
"""server_instance_name"""
"""exa_jdbc_type"""
"""SQL Server"""
"""database_name"""
]
Fields = [
""""+event_time"+:"+({time}[^"]+)"""
""""+server_principal_name"+:"+(({domain}[^"]+?)\\+({user}[\w\.\-]{1,40}\$?)|({db_user}[^"]+))"""
""""+server_instance_name"+:"+({dest_host}[\w\-.]+)"""
""""+statement"+:"+({db_query}.+?)\s*"+"""
""""+server_principal_sid"+:"+\s*({db_user_sid}.+?)\s*"+"""
""""+action_id"+:"+({db_operation}.+?)\s*"+"""
""""+database_name"+:"+({db_name}[^"]+)"+,"""
""""+schema_name"+:"+({schema_name}[^"]+)"+,"""
""""+object_name"+:"+({table_name}[^"]+)"+,"""
""""+succeeded"+:"?({result}[^\s,]+)"""
]
ParserVersion = "v1.0.0"


}
```