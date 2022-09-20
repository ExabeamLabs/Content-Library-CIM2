#### Parser Content
```Java
{
Name = imperva-securesphere-leef-database-query-success-query
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "dd MMMM yyyy HH:mm:ss"
Conditions = [
  """Authenticated=True"""
  """Event Type=Query"""
  """LEEF:"""
  """|SecureSphere|"""
  """User Type=Valid|"""
]
Fields = [
  """\|devTime=({time}\d+ \w+ \d+ \d\d:\d\d:\d\d)"""
  """usrName =(({domain}[^\\|]+)(\\))?({user}[^|]+)"""
  """ApplicationName =({app}[^|]+)"""
  """Service Name =({service_name}[^|]+)"""
  """Server Group=({server_group}[^|]+)"""
  """Database=({db_name}[^|]+)"""
  """src=((?=0\.0\.0\.0)|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))"""
  """dst=((?=0\.0\.0\.0)|({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))"""
  """\|Operation=(?: |({db_operation}[^|]+))"""
  """\|Response Size=({response_size}\d+)"""
]
DupFields = [
  "src_ip->host"
]
ParserVersion = "v1.0.0"


}
```