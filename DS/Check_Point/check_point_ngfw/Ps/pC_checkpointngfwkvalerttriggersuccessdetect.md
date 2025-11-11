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
    """\Wtime:({time}\d{10})""",
    """\W({host}[\w\-.]+) CheckPoint""",
    """\Wsrc:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """({result}Detect)""",
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
    """originsicname:({user_ou}[^"]+)""",
    """\Wdescription:({additional_info}[^"]+)""",
    """\Wprotection_name:({alert_name}[^"]+)""",
    """\Wpolicy_name=({rule}[^"]+?)\\\]"""
  ]


}
```