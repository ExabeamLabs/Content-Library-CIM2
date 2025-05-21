#### Parser Content
```Java
{
Name = postgresql-p-str-database-query-success-logaudit
 Vendor = PostgreSQL
 Product = PostgreSQL
 ParserVersion = "v1.0.0"
 TimeFormat = ["yyyy-MM-dd HH:mm:ss"]
 Conditions = [""":LOG: AUDIT: SESSION""", """]:""" ]
 Fields =[
   """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s*\w\w\w:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\(({src_port}\d+)\))?"""
   """AUDIT: SESSION,([^,]*,){6}({db_query}[^";]+);?,(\d+)?"""
   """\):({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({db_name}[^:]+):[^:]+:LOG: AUDIT:"""
 ]


}
```