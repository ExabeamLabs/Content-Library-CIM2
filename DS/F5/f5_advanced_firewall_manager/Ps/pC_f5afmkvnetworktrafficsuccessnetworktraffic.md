#### Parser Content
```Java
{
Name = f5-afm-kv-network-traffic-success-networktraffic
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 Advanced Firewall Manager
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """device_vendor="F5"""", """translated_vlan="""", """acl_policy_type="""" ]
  Fields = [
    """\Wacl_rule_name="({rule}[^"]+)""",
    """\Waction="({action}[^"]+)""",
    """\Whostname="({host}[^"]+)""",
    """\Wdest_ip="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wdest_port="({dest_port}\d+)""",
    """\Wsource_ip="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wsource_port="({src_port}\d+)""",
    """\Wdate_time="({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """\Wtranslated_dest_ip="({dest_translated_ip}[a-fA-F\d.:]+)""",
    """\Wtranslated_dest_port="({dest_translated_port}\d+)""",
    """\Wtranslated_source_ip="({src_translated_ip}[a-fA-F\d.:]+)""",
    """\Wtranslated_source_port="({src_translated_port}\d+)""",
    """\Wip_protocol="({protocol}[^"]+)""",
    """\Werrdefs_msg_name="({event_name}[^"]+)""",
  ]


}
```