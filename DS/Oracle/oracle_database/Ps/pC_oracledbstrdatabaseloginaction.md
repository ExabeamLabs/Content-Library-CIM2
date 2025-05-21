#### Parser Content
```Java
{
Name = oracle-db-str-database-login-action
ParserVersion = v1.0.0
Vendor = Oracle
Product = Oracle Database
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Oracle Audit"""
"""ACTION:"""
"""USERID:"""
"""LENGTH:"""
]
Fields = [
"""\d\d:\d\d:\d\d\s({host}[^\s]+)"""
"""SESSIONID:\[\d+\]\s*\"+({session_id}[^\":]+)"""
"""USERID:\[\d+\]\s*\"+({db_user}[^\":]+)"""
"""USERHOST:\[\d+\]\s*\"+({src_host}[^\":]+)"""
"""RETURNCODE:\[\d+\]\s*\"+({result}[^\":]+)"""
"""OBJ\$+NAME:\[\d+\]\s*\"+({db_name}[^\":]+)"""
"""OS\$+USERID:\[\d+\]\s*\"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""DBID:\[\d+\]\s*\"+({db_id}[^\":]+)"""
"""COMMENT\$+TEXT:\[\d+\]\s*.+?PROTOCOL=({protocol}\w+)"""
"""COMMENT\$+TEXT:\[\d+\]\s*.+?HOST=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""COMMENT\$+TEXT:\[\d+\]\s*.+?PORT=({dest_port}\d+)"""
"""ACTION:\[\d+\]\s+"+({db_operation}\d{1,3})""""
]


}
```