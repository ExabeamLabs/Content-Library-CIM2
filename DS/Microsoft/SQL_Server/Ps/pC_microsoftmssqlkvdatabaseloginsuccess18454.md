#### Parser Content
```Java
{
Name = microsoft-mssql-kv-database-login-success-18454
Vendor = "Microsoft"
Product = "SQL Server"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
  """EventCode=18454"""
  """Keywords=Audit Success"""
  """Login succeeded"""
]
Fields = [
  """\WComputerName =({host}[\w\-\.]+)\s*(\w+=|$)"""
  """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (AM|am|PM|pm))\s*(\w+=|$)"""
  """\WMessage=.*?\Wuser\s*'(({domain}[^\\]+)(\\)+)?({user}[^\\]+)'"""
  """\WSourceName =({service_name}.+?)\s*(\w+=|$)"""
  """\[CLIENT:\s+({src_ip}[a-fA-F\d:\.]+)\]"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```