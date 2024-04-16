#### Parser Content
```Java
{
Name = "ibm-guardium-cef-alert-trigger-success-cmealert"
Vendor = "IBM"
Product = "Guardium"
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "epoch"]
Conditions = [
"""|IBM|Guardium|"""
"""cs3Label=DatabaseName"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\scs5=(({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)|({table_name}\w+))"""
"""\ssuser=({user}[\w\.\-]{1,40}\$?)\s*\w+="""
"""\sduser=(|({db_user}.+?))\s*\w+="""
"""\scs3=(?: |({db_name}.+?))\s*\w+="""
"""\scs2=({server_group}.+?)\s*\w+="""
"""\ssrc=(0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sshost=(({domain}[^=\\\/]+)[\\\/]+)?({src_host}[^\s\\\/=]+)"""
"""CEF.+?([^|]+\|){5}({alert_name}[^|]+)"""
"""CEF.+?([^|]+\|){6}({alert_severity}[^|]+)"""
"""\sdhost=({dest_host}[\w\-.]+)"""
"""\scs6=.*?({db_operation}(?i)(insert|delete|truncate|drop|alter|create|update|enable|disable|merge|delete|merge|select|dbcc))"""
"""\scs6=\s*({db_query}.+?)\s+\w+="""
"""\scn3=\-?({response_size}\d+)\s+\w+="""
"""\scs4=(|({process_name}.+?))\s+\w+="""
"""\sdvchost=(localhost|({host}[\w\-.]+))"""
]
DupFields = [
"alert_name->alert_type"
"db_user->account"
"db_query->additional_info"
]
ParserVersion = "v1.0.0"


}
```