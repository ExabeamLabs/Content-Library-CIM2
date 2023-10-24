#### Parser Content
```Java
{
Name = ibm-guardium-cef-database-query-success-command
Vendor = "IBM"
Product = "Guardium"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """|IBM|Guardium|"""
  """cs3Label=Command"""
]
Fields = [
  """\sduser=(?:[^\\]*\\)?({db_user}.+?)\s+(\w+=|$)"""
  """\ssuser=((?:[^\s]+)?[\\\/])?({user}[\w\.\-]{1,40}\$?)\s+(\w+=|$)"""
  """\scs5=(?: |({db_name}.+?))\s+(\w+=|$)"""
  """\scs2=({server_group}.+?)\s+(\w+=|$)"""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sshost=({src_host}[^\s]+)"""
  """\scs3=({db_operation}.+?)\s+(\w+=|$)"""
  """\scn1=({response_size}\d+)"""
  """sessionStart="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
]
DupFields = [
  "db_user->account"
]
ParserVersion = "v1.0.0"


}
```