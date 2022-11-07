#### Parser Content
```Java
{
Name = imperva-securesphere-kv-database-login-success-login-1
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """Imperva |"""
  """operationname=Login"""
  """authenticated=True"""
]
Fields = [
  """\ssrc=({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})"""
  """\sspt=({src_port}\d+)"""
  """\sdst=({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})"""
  """\sdpt=({dest_port}\d+)"""
  """\sprotocol=({protocol}.*?)\s\w+="""
  """\sservicename=({service_name}.*?)\s\w+="""
  """\sservergroup=({server_group}[^\s]+)"""
  """\sappname=({app}.*?)\s\w+="""
  """\sauthenticated=({result}\s\w+=)"""
  """\ssrchostname=({src_host}[^\s]+)"""
  """\sdbname=({db_name}[^\s]+)"""
  """\sschemaname=({db_schema}[^\s]+)"""
  """\sresponsesize=({response_size}\d*)\s\w+="""
  """\sosuser=({user}[^\s]+])"""
  """\sduser=({db_user}[^\s]+)"""
]
DupFields = [
  "db_user->account"
  "user->user"
]
ParserVersion = "v1.0.0"


}
```