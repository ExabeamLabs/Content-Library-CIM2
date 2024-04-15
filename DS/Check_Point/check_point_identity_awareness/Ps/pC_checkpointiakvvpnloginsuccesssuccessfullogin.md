#### Parser Content
```Java
{
Name = "checkpoint-ia-kv-vpn-login-success-successfullogin"
Vendor = "Check Point"
Product = "Check Point Identity Awareness"
TimeFormat = "epoch"
Conditions = [
  """product=Identity Awareness"""
  """|auth_status=Successful Login|"""
]
Fields = [
  """"time=({time}\d{13})"""
  """\|hostname=({host}.+?)\s*\|"""
  """(U|u)ser=(-|({full_name}[^\(]+)\s+\(({user}[^\)]+))"""
  """\|src_user_group=({user_group_name}.+?)\s*\|"""
  """\|src_machine_name=({src_host}[^\|]+)"""
  """\|src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\|endpoint_ip=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\|ifdir=({direction}[^\|]+)"""
  """\|logid=({event_id}[^\|]+)"""
  """\|loguid=({log_uid}[^\|]+)"""
  """\|origin=({origin_ip}[^\|]+)"""
  """\|originsicname=({user_ou}[^\|]+)"""
  """\|auth_method=({auth_method}[^\|]+)"""
  """\|auth_status=({result}[^\|]+)"""
  """\|domain_name=({domain}[^\|]+)"""
  """({action}Successful)"""
]
ParserVersion = "v1.0.0"


}
```