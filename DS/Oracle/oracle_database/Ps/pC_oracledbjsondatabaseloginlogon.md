#### Parser Content
```Java
{
Name = "oracle-db-json-database-login-logon"
Vendor = "Oracle"
Product = "Oracle Database"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""os_username"""
""""dbid"""
""""LOGON"""
]
Fields = [
""""dbid\\?"+:\\?"+({db_id}[^"\\]+)"""
"""HOST=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""userhost\\?"+:\\?"+({src_host}[^"\\]+)"""
""""userhost"+:"+({domain}[^"\\]+)\\{1,2}({src_host}[^"\\]+)""""
""""terminal\\?"+:\\?"+({terminal}[^"\\]+)"""
""""+timestamp"*:"*({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""""+timestamp"*:"*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
""""username\\?"+:\\?"+({db_user}[^"\\]+)"""
""""os_username\\?"+:\\?"+({user}[\w\.\-]{1,40}\$?)"""
"""PROTOCOL=({protocol}\w+)"""
""""returncode\\?"+:\\?"+({return_code}[^"\\]+)"""
""""exa_jdbc_database":"({db_name}[^"]+)""""
""""exa_jdbc_type":"({app}[^"]+)""""
""""exa_jdbc_hostname":"({dest_host}[^"]+)""""
""""exa_jdbc_port":"({dest_port}\d+)""""
]
DupFields = [
"user->user"
"db_user->account"
]
ParserVersion = "v1.0.0"


}
```