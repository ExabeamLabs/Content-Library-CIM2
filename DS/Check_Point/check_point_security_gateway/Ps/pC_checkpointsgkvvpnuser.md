#### Parser Content
```Java
{
Name = "checkpoint-sg-kv-vpn-user"
Vendor = "Check Point"
Product = "Check Point Security Gateway"
TimeFormat = "epoch_sec"
Conditions = [
  """product=Mobile Access"""
  """cvpn_category"""
  """user="""
]
Fields = [
  """\Wtime=({time}\d{10})"""
  """\Whostname=({host}[\w\-.]+)"""
  """\Waction=({operation}[^\|]+?)\s*\|"""
  """\Wstatus=({result}[^\|]+?)\s*\|"""
  """\Wuser=(({last_name}[^,\|\(\)]+),\s*({first_name}[^,\|\(\)]+?)\s*\(({user}[\w\.\-]{1,40}\$?)\)|({=user}[^\|\s\)]+))\s*\|"""
  """\Wreason=({failure_reason}[^\|]+?)\s*\|"""
  """\Wservice=({dest_port}\d+)\s*\|"""
  """\Whost_ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wos_name=({os}[^\|]+?)\s*\|"""
  """\Wlogin_option=({auth_type}[^\|]+?)\s*\|"""
]
ParserVersion = "v1.0.0"


}
```