#### Parser Content
```Java
{
Name = postgresql-p-str-database-activity-fail-error
 Vendor = PostgreSQL
 Product = PostgreSQL
 ParserVersion = "v1.0.0"
 TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
 Conditions = [ """ERROR:""","""pid=""","""db=""" ]
 Fields =[
   """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s*\w\w\w:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\(({src_port}\d+)\))?"""
   """:({operation_type}ERROR):\s*({operation}[^:"]+)"""
   """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,6}Z)"""
   """({operation_type}ERROR):\s*({operation}[^:"]+)"""
   """\):({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({db_name}[^:]+):\["""
   """user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
   """db=({db_name}[^,]+)"""
   """client=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\(({src_port}\d+)\))?"""
 ]


}
```