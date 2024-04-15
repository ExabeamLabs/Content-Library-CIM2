#### Parser Content
```Java
{
Name = "imperva-securesphere-kv-database-query-success-query-1"
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Imperva |"""
"""rawdata="""
"""eventtype=Query"""
]
Fields = [
"""\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sspt=({src_port}\d+)"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sdpt=({dest_port}\d+)"""
"""\sprotocol=({protocol}.*?)\s\w+="""
"""\sservicename=({service_name}.*?)\s\w+="""
"""\sappname=({app}.*?)\s\w+="""
"""\seventtype=({event_category}.*?)\s\w+="""
"""\soperationname=({db_operation}.*?)\s\w+="""
"""\ssrchostname=({src_host}[^\s]+)"""
"""\sdbname=({db_name}[^\s]+)"""
"""\sschemaname=({db_schema}[^\s]+)"""
"""\sresponsesize=({response_size}\d*)\s\w+="""
"""\sosuser=({user}[^\s]+)"""
"""\sduser=({db_user}[^\s]+)"""
"""\sobjectname=({object_name}[^\s]+)"""
"""\srawdata=#\(({db_query}[^\)]+)"""
]
DupFields = [
"db_user->account"
"user->user"
]
ParserVersion = "v1.0.0"


}
```