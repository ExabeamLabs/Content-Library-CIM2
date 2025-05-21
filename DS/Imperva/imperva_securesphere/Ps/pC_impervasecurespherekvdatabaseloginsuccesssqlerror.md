#### Parser Content
```Java
{
Name = "imperva-securesphere-kv-database-login-success-sqlerror"
 Vendor = "Imperva"
 Product = "Imperva SecureSphere"
 TimeFormat = "yyyy-MM-dd HH:mm:ss"
 Conditions = [
   """imperva_version="""
   """event_type="""
   """sql_error="""
 ]
 Fields = [
   """(,\s+|,\s*)dest_ip=\s*({host}\S+?)\s*(,|$)"""
   """(,\s+|,\s*)hostname=\s*({host}[\w\.-]+)\s*(,|$)"""
   """=(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec)(  \d| \d\d) \d{1,2}:\d\d:\d\d\s+({host}[\w\.-]+)"""
   """(,\s+|,\s*)src_ip=\s*(0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*(,|$)"""
   """(,\s+|,\s*)dest_ip=\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s*(,|$)"""
   """(,\s+|,\s*)hostname=\s*({dest_host}[\w\.-]+)\s*(,|$)"""
   """(,\s+|,\s*)event_type=\s*(|({event_category}.+?))\s*(,|$)"""
   """(,\s+|,\s*)database_user=\s*(({domain}[^,]+?)\\)?({db_user}[^\s,][^,@]*?)\s*(,|$)"""
   """(,\s+|,\s*)database_user=\s*({db_user}[^\s\\,@][^\\,@]*?)(@({domain}[^,\s]+))?\s*(,|$)"""
   """(,\s+|,\s*)source_application=\s*(|({app}[^@]+?)(\s*@\s*({src_host}[\w\.-]+).*?)?)\s*(,|$)"""
   """(,\s+|,\s*)application_name=\s*(|({app}.+?))\s*(,|$)"""
   """({db_name}database)"""
   """(,\s+|,\s*)database=\s*(|({db_name}.+?))\s*(,|$)"""
   """(,\s+|,\s*)response_size=\s*(|({response_size}\d+))\s*(,|$)"""
   """(,\s+|,\s*)sql_error=\s*(|({sql_error}.+?))\s*(,|$)"""
   """(,\s+|,\s*)rawquery=[^,]*({db_operation}(insert|delete|truncate\s+\w+|drop\s+\w+|alter\s+\w+|create\s+\w+|update|enable\s+\w+|disable\s+\w+|merge|delete|select|dbcc))"""
   """(,\s+|,\s*)operation=\s*(|(L|l)ogin|(L|l)ogout|({db_operation}.+?))\s*(,|$)"""
   """(,\s+|,\s*)affected_rows=\s*(|({sql_count}\d+))\s*(,|$)"""
   """(,\s+|,\s*)rawquery=\s*(|({db_query}.+?))\s*(,\s*\w+=|$)"""
   """(,\s+|,\s*)schema=\s*(|({db_schema}.+?))\s*(,|$)"""
   """\Wos_user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
 ]
 DupFields = [
   "db_user->account"
 ]
 ParserVersion = "v1.0.0"


}
```