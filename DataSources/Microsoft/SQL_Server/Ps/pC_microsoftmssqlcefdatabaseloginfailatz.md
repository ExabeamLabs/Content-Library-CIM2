#### Parser Content
```Java
{
Name = microsoft-mssql-cef-database-login-fail-atz
ParserVersion = v1.0.0
Vendor = Microsoft
Product = SQL Server
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Microsoft|SQL Server|"""
""":18456|Login failed"""
]
Fields = [
"""\Wrt=({time}\d{10,13})"""
"""\Wsuser=(n\/a|(({domain}[^=\\\/]+)[\\\/]+)?({user}[^=\\\/]+?))(\s+\w+=|\s*$)"""
"""Reason:\s*({failure_reason}[^;\.]+)"""
"""src=({src_ip}[A-Fa-f:\d\.]+)"""
"""externalId=({event_code}18456)"""
"""\ssourceServiceName =({service_name}[^=]+?)\s*\w+="""
"""\Wdvchost=({dest_host}[\w\-.]+)"""
"""\sahost=({host}[^=]+?)(\s*[\w\.]+=)"""
"""\sshost=({src_host}[\w\.\-]+?)\s*[\w\-\.]+="""
]


}
```