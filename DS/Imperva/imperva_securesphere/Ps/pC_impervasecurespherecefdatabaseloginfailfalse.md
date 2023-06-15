#### Parser Content
```Java
{
Name = imperva-securesphere-cef-database-login-fail-false
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
  """operation="Login""""
  """OperationType=""""
  """databaseName =""""
  """|Imperva """
  """|SecureSphere|"""
  """userAuth="False""""
]
Fields = [
  """createTime="({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""""
  """({event_name}Login failed for user)"""
  """({event_name}logon denied)"""
  """({result}failed|denied)"""
  """\WdatabaseName ="(|({db_name}[^"]+))""""
  """\WsrcHost="(|({src_host}[^"]+))""""
  """\WdbUsername="(|(?i)(nt authority\\anonymous logon)|({domain}[^"\\]+)\\)?(|({db_user}[^"\\]+))""""
  """\WosUser="(|({user}[^"]+))""""
  """\WserviceName ="(|({service_name}[^"]+))""""
  """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wsrc=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  """\WappName ="(|({app}[^"]+))""""
  """\WschemaName ="(|({db_schema}[^"]+))""""
  """errorValue="({result_reason}[^"]+)\.?""""
]
DupFields = [
  "db_user->account"
]
ParserVersion = "v1.0.0"


}
```