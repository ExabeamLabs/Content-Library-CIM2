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
  """\sos-user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\sapplication-name=({app}[^,]+)"""
  """\sservice-name=({service_name}[^,]+)"""
  """\sserver-group=({server_group}[^,]+)"""
  """\sdatabase=(?: |({db_name}[^,]+))"""
  """\ssource-ip=(?:0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  """\sdest-ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\ssource-host=({src_host}[^,]+)"""
]
DupFields = [
  "db_user->account"
]
ParserVersion = "v1.0.0"


}
```