#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-network-traffic-fail-aclmatch
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "epoch_sec"
  Conditions = [ """ CheckPoint """, """product:"Syslog"""", """action:"Reject"""", """attack:"ACL match"""" ]
  Fields = [
    """\Wtime:"({time}\d{10})""",
    """\W({host}[\w\-.]+) CheckPoint""",
    """({action}Reject)""",
    """\Wsyslog_severity:"({alert_severity}[^"]+)"""",
    """\Worigin:"({origin_ip}[A-Fa-f\d\.:]+)"""",
    """\Wproduct:"({product_name}[^"]+)"""",
    """\Wsrc:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """\Wdst:"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """\Wproto:"({protocol}\d+)"""",
    """\Ws_port:"({src_port}\d+)"""",
    """\Wattack:"({attack}[^"]+)"""",
    """\Wdestination_interface:"({dest_interface}[^"]+)"""",
    """ASA-5-106100:\s({additional_info}[^"]+?)\s*""""
  ]
  ParserVersion = v1.0.0


}
```