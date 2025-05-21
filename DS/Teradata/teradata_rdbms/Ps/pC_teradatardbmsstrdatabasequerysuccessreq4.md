#### Parser Content
```Java
{
Name = "teradata-rdbms-str-database-query-success-req4"
Vendor = "Teradata"
Product = "Teradata RDBMS"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""teradata"""
"""[TERADATA]"""
"""REQ4"""
]
Fields = [
"""({task_id}REQ4)[\s(#)]{0,4}({site_id}\S+)[\s(#)]{0,4}({user}[\w\.\-\!\#\^\~]{1,40}\$?)[\s(#)]{0,4}({account}\S+)[\s(#)]{0,4}({time}\d\d\d\d-\d\d-\d\d\s*\d\d:\d\d:\d\d)[\s(#)]{0,4}(?:Unavailable|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)[\s(#)]{0,5}({query_id}\d+)[\s(#)]{0,4}({db_query}[^;]+)[\s;(#)]*(?:\?|({db_name}[^(#)]+))[\s(#)]{0,4}(?:[^(#)]+)[\s(#)]{0,4}(?:\?|({db_object}[^(#)]+))[\s(#)]{0,4}(?:\s|({error_info}[^(#)]+))[\s(#)]{0,4}({error_code}[\d]+)"""
]
ParserVersion = "v1.0.0"


}
```