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
    """\WSrcIP:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\WDstIP:\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
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
    """\sDNSRecordType:\s*({dns_query_type}[^,]+)""",
    """URLCategory:\s*({category}[^,]+)""",
    """\WURLReputation:\s*({reputation}[^,]+?)(,|\s*$)""",
  ]
  ParserVersion = "v1.0.0"


}
```