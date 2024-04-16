#### Parser Content
```Java
{
Name = microsoft-mssql-cef-database-login-success-loginsucceeded
Vendor = Microsoft
Product = MSSQL
TimeFormat = "epoch"
Conditions = [
  """|Microsoft|SQL Server|"""
  """|LOGIN SUCCEEDED|"""
  """outcome=true"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvchost=({host}[^\s]+)"""
  """\sduser=({user}[\w\.\-]{1,40}\$?)\s+\w+="""
  """\sdntdom=({domain}.+?)\s+\w+="""
  """\ssourceServiceName =(?: |({service_name}.+?))\s+\w+="""
  """\scs3=(?: |({db_name}.+?))\s+\w+="""
  """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sdhost=({dest_host}[\w\-.]+)"""
]
ParserVersion = "v1.0.0"


}
```