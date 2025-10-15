#### Parser Content
```Java
{
Name = "oracle-db-json-database-modify-success-fga"
Vendor = "Oracle"
Product = "Oracle Database"
ExtractionType = json
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""action_name":"UPDATE""""
""""object_schema":""""
""""return_code":""""
]
Fields = [
"""exa_json_path=$.event_timestamp,exa_field_name=time"""
"""exa_json_path=$.action_name,exa_field_name=db_operation"""
"""exa_json_path=$.return_code,exa_field_name=return_code"""
"""exa_json_path=$.os_username,exa_field_name=user"""
"""exa_json_path=$.dbusername,exa_field_name=db_user"""
"""exa_json_path=$.dbusername,exa_field_name=account"""
"""exa_regex=IP_ADDRESS=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$.userhost,exa_regex=(({domain}[^\\]+)[\\]+)?({src_host}[^"]+)"""
"""exa_json_path=$.object_schema,exa_field_name=db_schema"""
"""exa_json_path=$.object_schema,exa_field_name=db_name"""
"""exa_json_path=$.object_name,exa_field_name=db_object"""
]
ParserVersion = "v1.0.0"


}
```