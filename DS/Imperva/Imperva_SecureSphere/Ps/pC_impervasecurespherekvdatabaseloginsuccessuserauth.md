#### Parser Content
```Java
{
Name = imperva-securesphere-kv-database-login-success-userauth
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """ Imperva Inc.|SecureSphere,"""
  """event-type=Login"""
  """user-authenticated=True"""
]
Fields = [
  """\sdb-user=({db_user}[^,]+)"""
  """\sos-user=({user}[^,]+)"""
  """\sapplication-name=({app}[^,]+)"""
  """\sservice-name=({service_name}[^,]+)"""
  """\sserver-group=({server_group}[^,]+)"""
  """\sdatabase=(?: |({db_name}[^,]+))"""
  """\ssource-ip=(?:0.0.0.0|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))"""
  """\sdest-ip=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\ssource-host=({src_host}[^,]+)"""
]
DupFields = [
  "db_user->account"
]
ParserVersion = "v1.0.0"


}
```