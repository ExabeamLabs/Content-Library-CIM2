#### Parser Content
```Java
{
Name = "imperva-securesphere-kv-database-query-success-databasequery"
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = ["dd MMM yyyy HH:mm:ss","dd MMMM yyyy HH:mm:ss"]
Conditions = [
""" os_user="""
""" dbName ="""
""" operation="""
""" query=""""
]
Fields = [
"""event_time=({time}\d\d \w+ \d\d\d\d \d\d:\d\d:\d\d)"""
"""\w+ \d+ \d\d:\d\d:\d\d ({host}[\w\-.]+)"""
"""user=({db_user}[^\s]+)"""
"""os_user=({user}[\w\.\-]{1,40}\$?)"""
"""source_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""destination_ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""dbName =({db_name}.+?)\s*(\w+=|$)"""
"""operation=({db_operation}.+?)\s*(\w+=|$)"""
"""query="({db_query}[^"]+)"""
"""response_size=({response_size}\d+)"""
]
DupFields = [
"db_user->account"
]
ParserVersion = "v1.0.0"


}
```