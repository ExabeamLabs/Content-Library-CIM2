#### Parser Content
```Java
{
Name = "cisco-fp-json-alert-trigger-success-sinkhole"
Vendor = "Cisco"
Product = "Cisco Firepower"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """IngressInterface:"""
  """Sinkhole:"""
  """ConnectType:"""
]
Fields = [
  """({host}[\w\.-]+)\s+SFIMS:""",
  """"host\":\"({host}[^\"]+)""",
  """Protocol:\s*({protocol}[^,]+)""",
  """SrcIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """DstIP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """SrcPort:\s*({src_port}\d+)""",
  """DstPort:\s*({dest_port}\d+)""",
  """IngressInterface:\s*({ingress_interface}[^,]+)""",
  """EgressInterface:\s*({egress_interface}[^,]+)""",
  """IngressZone:\s*({ingress_zone}[^,]+)""",
  """EgressZone:\s*({egress_zone}[^,]+)""",
  """Policy:\s*({alert_type}[^,]+)""",
  """ConnectType:\s*({connection_type}[^,]+)""",
  """AccessControlRuleName:\s*({rule}[^,]+)""",
  """AccessControlRuleAction:\s*({result}[^,]+)""",
  """UserName:\s*(No Authentication Required|({user}[\w\.\-]{1,40}\$?))""",
  """UserAgent:\s*({user_agent}.+?), Client:""",
  """ApplicationProtocol:\s*({app_protocol}[^,]+)""",
  """WebApplication:\s*({web_application}[^,]+)""",
  """InitiatorPackets:\s*({initiator_packets}[^,]+)""",
  """ResponderPackets:\s*({responder_packets}\d+)""",
  """InitiatorBytes:\s*({bytes_in}\d+)""",
  """ResponderBytes:\s*({bytes_out}\d+)""",
  """NAPPolicy:\s*({nap_policy}[^,]+)""",
  """DNSResponseType:\s*({response_type}[^,]+)""",
  """ReferencedHost:\s*({dest_host}[\w\-.]+)""",
  """URL:\s*({url}[^\s\"]+)""",
  """\W({event_category}Connect)Type:\s*({subtype}[^,]+?)(,|\s*$)""",
  """\WICMPType:\s*({icmp_type}[^,]+?)(,|\s*$)""",
  """\WICMPCode:\s*({icmp_code}\d)""",
  """\WTCPFlags:\s*({tcp_flags}[^,]+?)(,|\s*$)""",
  """\WURLCategory:\s*(Unknown|({category}[^,]+?))(,|\s*$)""",
  """\WURLReputation:\s*({reputation}[^,]+?)(,|\s*$)"""
]
DupFields = [
  "rule->alert_name"
  "user_agent->additional_info"
]
ParserVersion = "v1.0.0"


}
```