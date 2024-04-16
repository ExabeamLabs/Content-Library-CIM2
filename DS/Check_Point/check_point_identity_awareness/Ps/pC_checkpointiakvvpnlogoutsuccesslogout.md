#### Parser Content
```Java
{
Name = "checkpoint-ia-kv-vpn-logout-success-logout"
Vendor = "Check Point"
Product = "Check Point Identity Awareness"
TimeFormat = "epoch_sec"
Conditions = [
  """product=Identity Awareness|action=Log Out"""
]
Fields = [
  """"time=({time}\d{10})\|"""
  """Origin=({origin_ip}[^\|]+)\|"""
  """(U|u)ser=(-|({full_name}[^\(]+)\s+\(({user}[\w\.\-]{1,40}\$?))"""
  """domain_name=(-|({domain}[^\|]+))\|"""
  """termination_reason=(-|({failure_reason}[^\|]+))\|"""
  """duration=(-|({session_duration}[^\|]+))\|"""
  """description=(-|({additional_info}[^\|]+))\|"""
  """\|hostname=({host}.+?)\s*\|"""
  """\|src_user_group=({user_group_name}.+?)\s*\|"""
  """\|src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\|ifdir=({direction}[^\|]+)"""
  """\|logid=({event_id}[^\|]+)"""
  """\|loguid=({log_uid}[^\|]+)"""
  """\|origin=({origin_ip}[^\|]+)"""
  """\|originsicname=({user_ou}[^\|]+)"""
]
ParserVersion = "v1.0.0"


}
```