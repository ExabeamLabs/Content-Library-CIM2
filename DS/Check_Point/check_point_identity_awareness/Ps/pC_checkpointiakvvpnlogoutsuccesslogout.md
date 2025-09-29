#### Parser Content
```Java
{
Name = "checkpoint-ia-kv-vpn-logout-success-logout"
Vendor = "Check Point"
Product = "Check Point Identity Awareness"
TimeFormat = "epoch_sec"
end_timeFormat = "epoch_sec"
start_timeFormat = "epoch_sec"
Conditions = ["""product:"Identity Awareness"""", """"Identity Collector"""", """"Log Out""""]
Fields = [
  """\stime:"({time}\d{10})""",
  """action:"({action}[^"]+)""",
  """ifdir:"({direction}[^"]+)""",
  """origin:"({host}[\w\-\.]+)""",
  """cu_rule_category:"({rule}[^"]+)""",
  """cu_rule_id:"({rule_id}[^"]+)""",
  """domain:"({domain}[^"]+)""",
  """duration:"({session_duration}[^"]+)""",
  """event_end_time:"({end_time}\d{10})""",
  """event_name:"({event_name}[^"]+)""",
  """event_start_time:"({start_time}\d{10})""",
  """identity_type:"({identity_type}[^"]+)""",
  """severity:"({severity}[^"]+)""",
  """snid:"({session_id}[^"]+)""",
  """src:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """src_user_name:"({full_name}[^\(]+)\s+\(({user}[\w\.\-]{1,40}\$?)\)""",
  """termination_reason:"({result_reason}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```