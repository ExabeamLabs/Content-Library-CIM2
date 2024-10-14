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
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sspt=({src_port}\d+)"""
  """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
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
  """\sosuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\sduser=({db_user}[^\s]+)"""
]
DupFields = [
  "db_user->account"
  "user->user"
]
ParserVersion = "v1.0.0"


}
```