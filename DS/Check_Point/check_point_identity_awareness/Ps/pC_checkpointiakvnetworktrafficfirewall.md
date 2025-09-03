#### Parser Content
```Java
{
Name = checkpoint-ia-kv-network-traffic-firewall
Vendor = "Check Point"
Product = "Check Point Identity Awareness"
TimeFormat = ["epoch_sec","yyyy-MM-dd HH:mm:ss"]
Conditions = [
  """|loguid="""
  """|origin="""
  """|product="""
]
Fields = [
  """\s+time=({time}\d{10})\|"""
  """({time}\d\d\d\d-\d\d-\d\d\s+\d\d:\d\d:\d\d)"""
  """hostname=({host}[^|]+)\|"""
  """layer_uuid=({user_uid}[^|]+)\|"""
  """rule_action=({action}[^|]+)\|"""
  """action=({action}[^\|]+)"""
  """origin=({origin_ip}[^|]+)\|"""
  """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\|"""
  """service=({dest_port}\d+)\|"""
  """service_id=({protocol}[^\-\|]+)"""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\||$)"""
  """conn_direction=({direction}[^|]+)\|"""
  """ifname=({src_interface}[^|]+)\|"""
  """\|logid=({event_id}[^\|]+)"""
  """\|loguid=({log_uid}[^\|]+)"""
  """\|s_port=({src_port}\d+)"""
  """(U|u)ser=(-|({full_name}[^\(]+)\s+\(({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    ]
ParserVersion = "v1.0.0"


}
```