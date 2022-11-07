#### Parser Content
```Java
{
Name = microsoft-mssql-cef-database-login-success-loginsucceeded
Vendor = Microsoft
Product = SQL Server
TimeFormat = "epoch"
Conditions = [
  """|Microsoft|SQL Server|"""
  """|LOGIN SUCCEEDED|"""
  """outcome=true"""
]
Fields = [
  """\srt=({time}\d+)"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvchost=({host}[^\s]+)"""
  """\sduser=({user}.+?)\s+\w+="""
  """\sdntdom=({domain}.+?)\s+\w+="""
  """\ssourceServiceName =(?: |({service_name}.+?))\s+\w+="""
  """\scs3=(?: |({db_name}.+?))\s+\w+="""
  """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdhost=({dest_host}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```