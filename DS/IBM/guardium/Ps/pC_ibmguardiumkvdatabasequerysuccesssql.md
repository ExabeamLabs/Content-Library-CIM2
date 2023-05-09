#### Parser Content
```Java
{
Name = ibm-guardium-kv-database-query-success-sql
Vendor = "IBM"
Product = "Guardium"
TimeFormat = "epoch"
Conditions = [
  """|IBM|Guardium|"""
  "cs3Label=Classification"""
  """act=SQL_"""
]
Fields = [
  """\|rt=({time}\d{13})"""
  """\ssuser=(:\w+=)?(?:|({user}.+?))\s*\w+="""
  """\sduser=(?:[^\\=]*\\)?(?:|({db_user}.+?))\s+(\w+=|$)"""
  """\scs2=({server_group}.+?)\s+(\w+=|$)"""
  """\ssproc=(?:|({app}.+?))\s*([-(#].+?)?\s*\w+="""
  """\ssrc=(?!0\.0\.0\.0)({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sdst=(?!0\.0\.0\.0)({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\smsg=.*?({db_operation}(?i)(insert|delete|truncate|drop|alter|create|update|enable|disable|merge|delete|merge|select|dbcc))"""
]
DupFields = [
  "db_user->account"
]
ParserVersion = "v1.0.0"


}
```