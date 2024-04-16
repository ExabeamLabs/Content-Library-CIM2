#### Parser Content
```Java
{
Name = "oracle-db-json-database-query-success-grantrole"
Vendor = "Oracle"
Product = "Oracle Database"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""os_username"""
""""dbid"""
""""sql_text"""
""""GRANT ROLE"""
]
Fields = [
    """exa_json_path=$..dbid,exa_field_name=db_id""",
    """exa_json_path=$..sql_text,exa_field_name=db_query""",
    """exa_json_path=$..userhost,exa_field_name=src_host""",
    """exa_json_path=$..terminal,exa_field_name=terminal""",
    """exa_json_path=$..timestamp,exa_field_name=time""",
    """exa_json_path=$..username,exa_field_name=db_user""",
    """exa_json_path=$..os_username,exa_field_name=user""",
    """exa_json_path=$..action_name,exa_field_name=db_operation"""
]
DupFields = [
"db_id->db_name"
"db_user->account"
]
ParserVersion = "v1.0.0"


}
```