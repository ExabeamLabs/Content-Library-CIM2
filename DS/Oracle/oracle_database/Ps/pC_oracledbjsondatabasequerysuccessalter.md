#### Parser Content
```Java
{
Name = "oracle-db-json-database-query-success-alter"
Vendor = "Oracle"
Product = "Oracle Database"
ExtractionType = json
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd HH:mm:ss.SSSSS", "yyyy-MM-dd HH:mm:ss.SSSSSS"]
Conditions = [
""""os_username"""
""""dbid"""
""""sql_text"""
""""ALTER """
]
Fields = [
"""exa_json_path=$..dbid,exa_field_name=db_id"""
"""exa_json_path=$..sql_text,exa_field_name=db_query"""
"""exa_json_path=$..userhost,exa_field_name=src_host"""
"""exa_json_path=$..userhost,exa_field_name=domain"""
"""exa_json_path=$..terminal,exa_field_name=terminal"""
"""exa_json_path=$.event_timestamp,exa_field_name=time"""
"""exa_json_path=$..timestamp,exa_field_name=time"""
"""exa_json_path=$..username,exa_field_name=db_user"""
"""exa_json_path=$..os_username,exa_field_name=user"""
"""exa_json_path=$..action_name,exa_field_name=db_operation"""
"""exa_json_path=$..exa_jdbc_database,exa_field_name=db_name"""
"""exa_json_path=$..exa_jdbc_type,exa_field_name=app"""
"""exa_json_path=$..exa_jdbc_hostname,exa_field_name=dest_host"""
"""exa_json_path=$..exa_jdbc_port,exa_field_name=dest_port"""
]
DupFields = [
"db_user->account"
]
ParserVersion = "v1.0.0"


}
```