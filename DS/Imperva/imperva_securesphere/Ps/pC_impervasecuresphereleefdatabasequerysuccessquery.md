#### Parser Content
```Java
{
Name = imperva-securesphere-leef-database-query-success-query
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "dd MMMM yyyy HH:mm:ss"
Conditions = [
  """Authenticated="""
  """Event Type=Query"""
  """LEEF:"""
  """|SecureSphere|"""
  """User Type="""
]
Fields = [
  """\|devTime=({time}\d+ \w+ \d+ \d\d:\d\d:\d\d)"""
  """usrName =(({domain}[^\\|]+)(\\))?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\|"""
  """ApplicationName =({app}[^|]+)"""
  """Service Name =({service_name}[^|]+)"""
  """Server Group=({server_group}[^|]+)"""
  """Database=({db_name}[^|]+)"""
  """src=((?=0\.0\.0\.0)|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  """dst=((?=0\.0\.0\.0)|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
  """\|Operation=(?: |({db_operation}[^|]+))"""
  """\|Response Size=({response_size}\d+)"""
  """Query=({db_query}[^"|]+)"""
  """Schema=({db_schema}[^\|]+)"""
  """Object name=({table_name}[^|]+)\|Object type=table"""
]
DupFields = [
  "src_ip->host"
]
ParserVersion = "v1.0.0"


}
```