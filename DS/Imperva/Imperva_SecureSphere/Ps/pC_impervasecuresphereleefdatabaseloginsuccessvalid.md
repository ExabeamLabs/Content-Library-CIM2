#### Parser Content
```Java
{
Name = imperva-securesphere-leef-database-login-success-valid
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "dd MMMM yyyy HH:mm:ss"
Conditions = [
  """Authenticated=True"""
  """Event Type=Login"""
  """LEEF:"""
  """|SecureSphere|"""
  """User Type=Valid|"""
]
Fields = [
  """\|devTime=({time}\d+ \w+ \d+ \d\d:\d\d:\d\d)"""
  """usrName =(({domain}[^\\|]+)(\\))?({user}[^|]+)"""
  """ApplicationName =({app}[^|]+)"""
  """src=((?=0\.0\.0\.0)|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))"""
  """dst=((?=0\.0\.0\.0)|({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))"""
  """Service Name =({service_name}[^|]+)"""
  """Server Group=({server_group}[^|]+)"""
  """Database=({db_name}[^|]+)"""
]
DupFields = [
  "src_ip->host"
]
ParserVersion = "v1.0.0"


}
```