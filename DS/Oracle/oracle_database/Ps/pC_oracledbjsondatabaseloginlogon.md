#### Parser Content
```Java
{
Name = "oracle-db-json-database-login-logon"
Vendor = "Oracle"
Product = "Oracle Database"
ExtractionType = json
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd HH:mm:ss.S", "yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd HH:mm:ss.SSSSS", "yyyy-MM-dd HH:mm:ss.SSSSSS"]
Conditions = [
""""os_username"""
""""dbid"""
""""LOGON"""
]
Fields = [
"""exa_json_path=$..dbid,exa_field_name=db_id"""
"""exa_regex=HOST=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$..userhost,exa_field_name=src_host"""
"""exa_json_path=$..userhost,exa_regex=(({domain}[^\\]+)[\\]+)?({src_host}[^"]+)"""
"""exa_json_path=$..terminal,exa_field_name=terminal"""
"""exa_json_path=$.event_timestamp,exa_field_name=time"""
"""exa_json_path=$..timestamp,exa_field_name=time"""
"""exa_json_path=$..username,exa_field_name=db_user"""
"""exa_json_path=$..os_username,exa_field_name=user"""
"""exa_regex=PROTOCOL=({protocol}\w+)"""
"""exa_json_path=$..return_code,exa_field_name=return_code"""
"""exa_json_path=$..returncode,exa_field_name=return_code"""
"""exa_json_path=$..exa_jdbc_database,exa_field_name=db_name"""
"""exa_json_path=$..exa_jdbc_type,exa_field_name=app"""
"""exa_json_path=$..exa_jdbc_hostname,exa_field_name=dest_host"""
"""exa_json_path=$..exa_jdbc_port,exa_field_name=dest_port"""
"""exa_json_path=$..action_name,exa_field_name=db_operation"""
"""exa_json_path=$..sessionid,exa_field_name=session_id"""
]
DupFields = [
"db_user->account"
]
ParserVersion = "v1.0.0"


}
```