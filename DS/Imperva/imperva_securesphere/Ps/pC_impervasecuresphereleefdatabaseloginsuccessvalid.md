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
  """usrName =(({domain}[^\\|]+)(\\))?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """ApplicationName =({app}[^|]+)"""
  """src=((?=0\.0\.0\.0)|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  """dst=((?=0\.0\.0\.0)|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
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