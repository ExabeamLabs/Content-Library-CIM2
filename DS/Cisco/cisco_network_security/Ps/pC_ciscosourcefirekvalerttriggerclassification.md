#### Parser Content
```Java
{
Name = cisco-sourcefire-kv-alert-trigger-classification
  ParserVersion = "v1.0.0"
  Product = Cisco Network Security
  Vendor = Cisco
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """SFIMS:""", """Classification:""", """Priority:""" ]
  Fields = [
    """({host}[\w\-.]+)\s+SFIMS:""",
    """\WMessage:\s*"({alert_name}[^"]+)""",
    """\WClassification:\s*({alert_type}[^,]+)\s*(,|$)""",
    """\WProtocol:\s*({protocol}[^,]+)\s*(,|$)""",
    """\WSrcIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\WDstIP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\WSrcPort:\s*({src_port}\d+)""",
    """\WDstPort:\s*({dest_port}\d+)""",
    """\WPriority:\s*({alert_severity}[^,]+)\s*(,|$)""",
    """\WUser:\s*(No Authentication Required|(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
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