#### Parser Content
```Java
{
Name = cisco-fp-kv-network-traffic-success-accesscontrolrule
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """ FirePower """, """Protocol="""", """AccessControlRuleName ="""", """AccessControlRuleAction="""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)\s+({host}[\w\.-]+)\s+FirePower""",
    """\WProtocol(:|=")\s*({protocol}[^,"]+)""",
    """\WSrcIP(:|=")\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\WDstIP(:|=")\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\WSrcPort(:|=")\s*({src_port}\d+)""",
    """\WDstPort(:|=")\s*({dest_port}\d+)""",
    """\WIngressZone(:|=")\s*({ingress_zone}[^,"]+)""",
    """\WEgressZone(:|=")\s*({egress_zone}[^,"]+)""",
    """\WPolicy(:|=")\s*({policy_name}[^,"]+)""",
    """\WAccessControlRuleName(:|=")\s*(Unknown|({rule}[^,"]+))""",
    """\WAccessControlRuleAction(:|=")\s*({result}[^,"]+)""",
    """\WUser(:|=")\s*(No Authentication Required|({user}[^,\s"]+))"""",
    """\WInitiatorPackets(:|=")\s*({initiator_packets}[^,"]+)""",
    """\WResponderPackets(:|=")\s*({responder_packets}\d+)""",
    """\WInitiatorBytes(:|=")\s*({bytes_in}\d+)""",
    """\WResponderBytes(:|=")\s*({bytes_out}\d+)""",
    """\WNAPPolicy(:|=")\s*({nap_policy}[^,"]+)""",
    """\WDNSResponseType(:|=")\s*({response_type}[^,"]+)""",
  ]
  DupFields = [ "result->action" ]


}
```