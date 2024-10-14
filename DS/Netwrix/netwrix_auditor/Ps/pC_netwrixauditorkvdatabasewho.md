#### Parser Content
```Java
{
Name = netwrix-auditor-kv-database-who
ParserVersion = "v1.0.0"
Vendor = Netwrix
Product = Netwrix Auditor
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""DataSource : SQL"""
"""Where :"""
"""Who :"""
]
Fields = [
"""When : ({time}[^\s]+)"""
"""What\s*:\s*(.+?\\+)?({db_name}[^\s]+)""",
"""Who\s*:\s*(({domain}[^\s]+)\\+)?(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""Where\s*:\s*({dest_host}[\w\-.]+)"""
"""Workstation\s*:\s*(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*Details\s*:"""
"""ObjectType\s*:\s*({additional_info}.+?)\s*\w+\s*:\s*"""
"""Device name:\s*\"*({service_name}[^\",\s]+)"""
"""Message\s*:\s*({result_reason}.+?)\s*\w+\s*:"""
"""DataSource\s*:\s*({app}.+?)\s*\w+\s*:"""
"""Application name:\s*({app}.+?)\s*$"""
]


}
```