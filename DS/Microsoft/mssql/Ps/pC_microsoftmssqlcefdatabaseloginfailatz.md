#### Parser Content
```Java
{
Name = microsoft-mssql-cef-database-login-fail-atz
ParserVersion = v1.0.0
Vendor = Microsoft
Product = MSSQL
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Microsoft|SQL Server|"""
""":18456|Login failed"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wsuser=(n\/a|(({domain}[^=\\\/]+)[\\\/]+)?({user}[^=\\\/]+?))(\s+\w+=|\s*$)"""
"""Reason:\s*({failure_reason}[^;\.]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""externalId=({event_code}18456)"""
"""\ssourceServiceName =({service_name}[^=]+?)\s*\w+="""
"""\Wdvchost=({dest_host}[\w\-.]+)"""
"""\sahost=({host}[^=]+?)(\s*[\w\.]+=)"""
"""\sshost=({src_host}[\w\.\-]+?)\s*[\w\-\.]+="""
]


}
```