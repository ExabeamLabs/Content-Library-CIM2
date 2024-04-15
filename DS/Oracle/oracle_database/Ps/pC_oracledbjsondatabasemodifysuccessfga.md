#### Parser Content
```Java
{
Name = "oracle-db-json-database-modify-success-fga"
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""action_name":"UPDATE""""
""""object_schema":""""
""""return_code":""""
]
Fields = [
""""event_timestamp":\"({time}[^\"]+)"""
""""action_name":\"({db_operation}[^\"]+)"""
""""return_code":\"({return_code}[^\"]+)"""
""""os_username":\"({user}[^\"]+)"""
""""dbusername":\"({db_user}[^\"]+)"""
"""IP_ADDRESS=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""userhost":\"({src_host}[^\"]+)"""
""""object_schema":\"({db_schema}[^\"]+)"""
""""object_name":\"({db_object}[^\"]+)"""
]
DupFields = [
 "db_user->account"
 "db_schema->db_name"
]
ParserVersion = "v1.0.0"


}
```