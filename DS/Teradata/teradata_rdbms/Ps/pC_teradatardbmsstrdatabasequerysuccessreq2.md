#### Parser Content
```Java
{
Name = "teradata-rdbms-str-database-query-success-req2"
Vendor = "Teradata"
Product = "Teradata RDBMS"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""teradata"""
"""[TERADATA]"""
"""REQ2"""
]
Fields = [
"""({task_id}REQ2)[\s(#)]{0,4}({site_id}\S+)[\s(#)]{0,4}({user}[\w\.\-\!\#\^\~]{1,40}\$?)[\s(#)]{0,4}({account}\S+)[\s(#)]{0,4}({time}\d\d\d\d-\d\d-\d\d\s*\d\d:\d\d:\d\d)[\s(#)]{0,4}(?:Unavailable|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)[\s(#)]{0,5}({session_id}[\d,]+)[\s(#)]{0,4}({query_id}\d+)[\s(#)]{0,4}({db_operation}\S+)[\s(#)]{0,4}({db_query}[^;]+)"""
]
ParserVersion = "v1.0.0"


}
```