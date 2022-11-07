#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-alert-trigger-success-detect
  ParserVersion = v1.0.0
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "epoch_sec"
  Conditions = [ """ CheckPoint """, """action:Detect""", """product=VPN-1 & FireWall-1""", """origin:""" ]
  Fields = [
    """\Wtime:({time}\d+)""",
    """\W({host}[\w\-.]+) CheckPoint""",
    """\Wsrc:({src_ip}[A-Fa-f:\d.]+)""",
    """\Wdst:({dest_ip}[A-Fa-f:\d.]+)""",
    """({action}Detect)""",
    """\Ws_port:({src_port}\d+)""",
    """\Wproto:({protocol}[^"]+)""",
    """\Wservice:({dest_port}\d+)""",
    """\Wseverity:({alert_severity}[^"]+)""",
    """\Wprotection_name:({protection_name}[^"]+)""",
    """\Wprotection_type:({alert_type}[^"]+)""",
    """\Worigin:({origin_ip}[A-Fa-f\d\.:]+)""",
    """\Worigin_?sic_?name:CN=({origin_name}[^",]+)""",
    """\Wproduct:({product_name}[^"]+)""",
    """\Wconfidence_level:({confidence_level}[^"]+)""",
    """\Wrule_uid:({rule_id}[^"]+)""",
    """\Wsmartdefense_profile:({smartdefense_profile}[^"]+)""",
    """ifdir:({direction}[^"]+)""",
    """originsicname:({user_ou}[^"]+)""",
    """\Wdescription:({additional_info}[^"]+)""",
    """\Wpolicy_name=({rule}[^"]+?)\\\]"""
  ]
  DupFields = ["protection_name->alert_name"]


}
```