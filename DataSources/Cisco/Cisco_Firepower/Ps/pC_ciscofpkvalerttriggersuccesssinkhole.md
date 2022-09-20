#### Parser Content
```Java
{
Name = cisco-fp-kv-alert-trigger-success-sinkhole
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [""" SFIMS: """, """ Sinkhole: """, """ OriginalClientIP: """]
  Fields = [
    """({host}[\w\-.]+)\s+SFIMS:""",
    """\WProtocol:\s*({protocol}[^,]+)\s*(,|$)""",
    """\WSrcIP:\s*({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """\WDstIP:\s*({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """\WSrcPort:\s*({src_port}\d+)""",
    """\WDstPort:\s*({dest_port}\d+)""",
    """\WIngressZone:\s*({ingress_zone}[^,]+)\s*(,|$)""",
    """\WEgressZone:\s*({egress_zone}[^,]+)\s*(,|$)""",
    """\WDE:\s*({engine_name}[^,]+)\s*(,|$)""",
    """\WRevision:\s*({revision}[^,]+)\s*(,|$)""",
    """\WPolicy:\s*({policy_name}[^,]+)\s*(,|$)"""
    """\WAccessControlRuleAction:\s*({action}[^,]+)""",
    """\WUserName:\s*({user}[^,]+)""",
    """InitiatorBytes:\s*({bytes_in}\d+)""",
    """\WResponderBytes:\s*({bytes_out}\d+)""",
    """NAPPolicy:\s*({nap_policy}[^,]+)""",
    """\sDNSQuery:\s*({query}[^,]+)""",
    """\WDNSResponseType:\s*({response_type}[^,]+)""",
    """\sDNSRecordType:\s*({query_type}[^,]+)""",
    """URLCategory:\s*({category}[^,]+)""",
    """\WURLReputation:\s*({reputation}[^,]+?)(,|\s*$)""",
  ]
  ParserVersion = "v1.0.0"


}
```