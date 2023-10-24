#### Parser Content
```Java
{
Name = "oracle-db-json-database-query-success-grantrole"
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""os_username"""
""""dbid"""
""""sql_text"""
""""GRANT ROLE"""
]
Fields = [
    """"dbid\\"+:\\"+({db_id}[^"\\]+)""",
    """"sql_text\\"+:\\"+({db_query}[^"\\]+)""",
    """HOST=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"userhost\\"+:\\"+({src_host}[^"\\]+)""",
    """"terminal\\"+:\\"+({terminal}[^"\\]+)""",
    """"timestamp\\"+:\\"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"username\\"+:\\"+({db_user}[^"\\]+)""",
    """"os_username\\"+:\\"+({user}[\w\.\-]{1,40}\$?)""",
    """"action_name\\"+:\\"+({db_operation}[^"\\]+)"""
]
DupFields = [
"db_id->db_name"
"user->user"
"db_user->account"
]
ParserVersion = "v1.0.0"


}
```