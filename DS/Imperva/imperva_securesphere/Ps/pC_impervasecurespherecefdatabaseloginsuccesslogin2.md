#### Parser Content
```Java
{
Name = imperva-securesphere-cef-database-login-success-login-2
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
  """operation="Login""""
  """OperationType=""""
  """databaseName =""""
  """|Imperva """
  """|SecureSphere|"""
  """userAuth="True""""
]
Fields = [
  """createTime="({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""""
  """({event_name}Login)"""
  """\WdatabaseName ="(|({db_name}[^"]+))""""
  """\WsrcHost="(|({src_host}[^"]+))""""
  """\WdbUsername="(|({domain}[^"\\]+)\\)?(|({db_user}[^"\\]+))""""
  """\WosUser="(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
  """\WserviceName ="(|({service_name}[^"]+))""""
  """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wsrc=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  """\WappName ="(|({app}[^"]+))""""
  """\WschemaName ="(|({db_schema}[^"]+))""""
]
DupFields = [
  "db_user->account"
]
ParserVersion = "v1.0.0"


}
```