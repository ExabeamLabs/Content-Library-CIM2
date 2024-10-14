#### Parser Content
```Java
{
Name = "ibm-guardium-leef-database-activity-success-ibm"
Vendor = "IBM"
Product = "Guardium"
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "MMM dd HH:mm:ss"]
Conditions = [
"""|IBM|Guardium|"""
"""Object/Field="""
"""App User Name ="""
]
Fields = [
"""({time}\w+\s+\d+ \d+:\d+:\d+)"""
""":\d+\s*({host}[^\s]+)\s*\w+:"""
"""\d\d:\d\d:\d\d\s*({host}[^\.]+)\.({domain}[^\.]+)\..*?(?=\sauditprocess)"""
"""Start\sTime=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""({process_name}[^\|]+)\|App\sUser\sName =({user}[\w\.\-\!\#\^\~]{1,40}\$?)\|Service\sName =({service_name}[^\|]+)\|Object\/Field=({db_object}[^\|]+)\|Sum\sOf\sRecord\sAffected=({sql_count}\d+)"""
]
DupFields = [
"user->db_user"
]
ParserVersion = "v1.0.0"


}
```