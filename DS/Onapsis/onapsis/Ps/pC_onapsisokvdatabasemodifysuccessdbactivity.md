#### Parser Content
```Java
{
Name = "onapsis-o-kv-database-modify-success-dbactivity"
Vendor = "Onapsis"
Product = "Onapsis"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""", db_table="""
""", action="""
""", user_name="""
""", user_id="""
]
Fields = [
"""<.*?>\w+ \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} ({host}[\w\.-]+?) ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""", user_name=\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*,"""
""", user_id=\s*({user_id}[^,]+?)\s*,"""
""", action=\s*({db_operation}[^,]+?)\s*,"""
""", db_table\s*=({table_name}[^,]+?)\s*,"""
""", ({additional_info}change\..+change\..+?="+.+?"+)"""
""", request_id=\s*({alert_id}[^,]+?)\s*,"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```