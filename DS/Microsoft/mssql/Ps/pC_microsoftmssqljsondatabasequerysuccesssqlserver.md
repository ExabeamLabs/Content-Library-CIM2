#### Parser Content
```Java
{
Name = "microsoft-mssql-json-database-query-success-sqlserver"
Vendor = "Microsoft"
Product = "MSSQL"
ExtractionType = json
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSSSSS"
Conditions = [
"""server_instance_name"""
"""exa_jdbc_type"""
"""SQL Server"""
"""database_name"""
]
Fields = [
  """exa_json_path=$.event_time,exa_field_name=time""",
  """exa_json_path=$.server_principal_name,exa_regex=(({domain}[^"]+?)\\+({user}[\w\.\-]{1,40}\$?)|({db_user}[^"]+))""",
  """exa_json_path=$.server_instance_name,exa_field_name=dest_host""",
  """exa_json_path=$.statement,exa_field_name=db_query""",
  """exa_json_path=$.server_principal_sid,exa_regex=({db_user_sid}.+?)\s*"+""",
  """exa_json_path=$.action_id,exa_field_name=db_operation""",
  """exa_json_path=$.database_name,exa_field_name=db_name""",
  """exa_json_path=$.schema_name,exa_field_name=schema_name""",
  """exa_json_path=$.object_name,exa_field_name=table_name""",
  """exa_json_path=$.succeeded,exa_field_name=result""",
]
ParserVersion = "v1.0.0"


}
```