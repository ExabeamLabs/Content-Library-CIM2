#### Parser Content
```Java
{
Name = "oracle-db-kv-database-login-fail-user"
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
Conditions = [
""" ACTION_NAME: """
""""LOGON""""
""" COMMENT_TEXT: """
""""Authenticated by:"""
]
Fields = [
"""OS_USERNAME:\s*"+({user}[^":]+)"""
"""\sUSERNAME:\s*"+({db_user}[^":]+)"""
"""USERHOST:\s*"+({dest_host}[^":]+)"""
"""TIMESTAMP:\s*"+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)"""
"""COMMENT_TEXT:\s*"+[^"]*?PROTOCOL=({protocol}\w+)"""
"""COMMENT_TEXT:\s*"+[^"]*?HOST=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""SESSIONID:\s*"+({session_id}[^":]+)"""
"""OS_PROCESS:\s*"+({process_id}\d+)"""
"""DBID:\s*"+({db_name}\d+)"""
]
DupFields = [
"user->user"
"db_user->account"
]
ParserVersion = "v1.0.0"


}
```