#### Parser Content
```Java
{
Name = postgresql-p-str-database-activity-success-postgresql
 Vendor = PostgreSQL
 Product = PostgreSQL
 ParserVersion = "v1.0.0"
 TimeFormat = ["yyyy-MM-dd HH:mm:ss"]
 Conditions = [ """"product":"PostgreSQL"""" ]
 Fields = [
   """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s*"""
   """Query Text:\s*({db_query}[^;]+)""""
   """error:\s*({result}[^"]+)"""
   """:\s*statement:\s*({db_query}[^;]+)"""
   """\):({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({db_name}[^:]+):[^:]+.+?statement:"""
 ]


}
```