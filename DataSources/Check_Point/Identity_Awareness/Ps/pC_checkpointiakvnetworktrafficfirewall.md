#### Parser Content
```Java
{
Name = checkpoint-ia-kv-network-traffic-firewall
Vendor = "Check Point"
Product = "Identity Awareness"
TimeFormat = "epoch_sec"
Conditions = [
  """|loguid="""
  """|origin="""
  """|product="""
]
Fields = [
  """"time=({time}\d{10})\|"""
  """hostname=({host}[^|]+)\|"""
  """layer_uuid=({user_uid}[^|]+)\|"""
  """rule_action=({action}[^|]+)\|"""
  """action=({action}[^\|]+)"""
  """origin=({origin_ip}[^|]+)\|"""
  """dst=({dest_ip}[^|]+)\|"""
  """service=({dest_port}\d+)\|"""
  """service_id=({protocol}[^|]+)\|"""
  """src=({src_ip}[^|]+)\|"""
  """ifdir=({direction}[^|]+)\|"""
  """ifname=({src_interface}[^|]+)\|"""
  """\|logid=({event_id}[^\|]+)"""
  """\|loguid=({log_uid}[^\|]+)"""
  """\|s_port=({src_port}\d+)"""
  """(U|u)ser=(-|({full_name}[^\(]+)\s+\(({user}[^\)]+))"""
]
ParserVersion = "v1.0.0"


}
```