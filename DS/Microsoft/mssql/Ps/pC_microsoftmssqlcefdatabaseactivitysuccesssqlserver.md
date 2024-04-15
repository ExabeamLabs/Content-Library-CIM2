#### Parser Content
```Java
{
Name = "microsoft-mssql-cef-database-activity-success-sqlserver"
Vendor = "Microsoft"
Product = "MSSQL"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Microsoft|SQL Server|"""
"""fileType=Security Audit"""
]
Fields = [
"""\ssuser=(({domain}[^=\\\/]+)[\\\/]+)?({user}[^\\\/=]+?)(\s+\w+=|\s*$)"""
"""CEF:([^\|]*\|){5}({reason}[^\|]+)"""
"""cs3=({service_name}[^\s]+)"""
"""\sdestinationServiceName =(|({service_name}.+?))(\s+\w+=|\s*$)"""
"""\sshost=(|({host}.+?))(\s+\w+=|\s*$)"""
"""\srt=({time}\d{13})"""
]
ParserVersion = "v1.0.0"


}
```