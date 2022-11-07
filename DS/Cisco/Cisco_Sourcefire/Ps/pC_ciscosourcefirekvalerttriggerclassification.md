#### Parser Content
```Java
{
Name = cisco-sourcefire-kv-alert-trigger-classification
  ParserVersion = "v1.0.0"
  Product = Cisco Sourcefire
  Vendor = Cisco
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """SFIMS:""", """Classification:""", """Priority:""" ]
  Fields = [
    """({host}[\w\-.]+)\s+SFIMS:""",
    """\WMessage:\s*"({alert_name}[^"]+)""",
    """\WClassification:\s*({alert_type}[^,]+)\s*(,|$)""",
    """\WProtocol:\s*({protocol}[^,]+)\s*(,|$)""",
    """\WSrcIP:\s*({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """\WDstIP:\s*({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""",
    """\WSrcPort:\s*({src_port}\d+)""",
    """\WDstPort:\s*({dest_port}\d+)""",
    """\WPriority:\s*({alert_severity}[^,]+)\s*(,|$)""",
    """\WUser:\s*(No Authentication Required|(({domain}[^\\]+)\\+)?({user}[^\s,]+))""",
    """\WIngressInterface:\s*({ingress_interface}[^,]+)\s*(,|$)""",
    """\WEgressInterface:\s*({egress_interface}[^,]+)\s*(,|$)""",
    """\WIngressZone:\s*({ingress_zone}[^,]+)\s*(,|$)""",
    """\WEgressZone:\s*({egress_zone}[^,]+)\s*(,|$)""",
    """\WDE:\s*({engine_name}[^,]+)\s*(,|$)""",
# gid is removed
    """\WSID:\s*({user_sid}[^,]+)\s*(,|$)""",
    """\WRevision:\s*({revision}[^,]+)\s*(,|$)""",
    """\WPolicy:\s*({policy_name}[^,]+)\s*(,|$)"""
    ]


}
```