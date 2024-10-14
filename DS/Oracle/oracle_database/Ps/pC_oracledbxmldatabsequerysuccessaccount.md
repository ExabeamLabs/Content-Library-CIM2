#### Parser Content
```Java
{
Name = "oracle-db-xml-databse-query-success-account"
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
"""<DB_User>"""
"""<OS_User>"""
"""<Userhost>"""
"""<OS_Process>"""
"""<DBID>"""
"""<Sql_Text>"""
]
Fields = [
"""<Extended_Timestamp>({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+\w)</Extended_Timestamp>"""
"""<DB_User>(\/|({db_user}.+?))</DB_User>"""
"""<OS_User>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</OS_User>"""
"""<Userhost>({src_host}[^\<]+)</Userhost>"""
"""<OS_Process>({process_id}\d+)</OS_Process>"""
"""<Session_Id>({session_id}\d+)</Session_Id>"""
"""<Returncode>({result}.+?)</Returncode>"""
"""PROTOCOL=({protocol}[^\)]+)"""
"""PORT=({src_port}\d+)"""
"""<DBID>({db_id}\d+)</DBID>"""
"""<Sql_Text>\s*({db_query}({db_operation}\w+)\s.+?)\s*</Sql_Text>"""
]
DupFields = [
"user->user"
"db_user->account"
"db_id->db_name"
]
ParserVersion = "v1.0.0"


}
```