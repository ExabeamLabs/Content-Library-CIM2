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
"""What\s*:\s*(.+?\+)?({db_name}[^\s]+)"""
"""Who\s*:\s*(({domain}[^\s]+)\\+)?(system|({user}[^\s]+))"""
"""Where\s*:\s*({dest_host}[\w\-.]+)"""
"""Workstation\s*:\s*(|({src_ip}[A-Fa-f:\d.]+))\s*Details\s*:"""
"""ObjectType\s*:\s*({additional_info}.+?)\s*\w+\s*:\s*"""
"""Device name:\s*\"*({service_name}[^\",\s]+)"""
"""Message\s*:\s*({result_reason}.+?)\s*\w+\s*:"""
"""DataSource\s*:\s*({app}.+?)\s*\w+\s*:"""
"""Application name:\s*({app}.+?)\s*$"""
]


}
```