#### Parser Content
```Java
{
Name = checkpoint-tp-kv-alert-trigger-success-smartdefense
  Product = Threat Prevention
  ParserVersion = v1.0.0
  Conditions = [ """product:""", """SmartDefense""", """CheckPoint""", """sequencenum""", """attack:""" ]

checkpoint-network-alert = {
  Vendor = Check Point
  TimeFormat = "epoch_sec"
  Fields = [
    """\Wtime:"({time}\d+)""",
    """\W({host}[\w\-.]+) CheckPoint""",
    """\Wuser:"({last_name}[^,]+),\s*({first_name}[\w\s]+\S)\s*\(({account}.+?)\)""",
    """\Wuser:"({first_name}[^\s,]+)\s+({last_name}[^,\(]+?)\s+\(({account}[^\(]+?)\)""",
    """\Wsrc:"({src_ip}[A-Fa-f:\d.]+)""",
    """\Wdst:"({dest_ip}[A-Fa-f:\d.]+)""",
    """\Waction:"({action}[^"]+)""",
    """\Ws_port:"({src_port}\d+)""",
    """\Wproto:"({protocol}[^"]+)""",
    """\Wservice:"({dest_port}\d+)""",
    """\Wseverity:"({alert_severity}[^"]+)""",
    """\Wmessage_info:"({alert_name}[^"]+)""",
    """\Wmessage_info:"({alert_type}[^"]+)""",
    """\Wprotection_name:"({protection_name}[^"]+)""",
    """\Wprotection_name:"({alert_name}[^"]+)""",
    """\Wprotection_type:"({alert_type}[^"]+)""",
    """\Wattack_info:"({attack_info}[^"]+)""",
    """\Wsrc_machine_name:"({src_host}[^"@]+)@({domain}[^"]+)""",
    """\Worigin:"({origin_ip}[^"]+)""",
    """\Worigin_?sic_?name:"CN=({origin_name}[^",]+)""",
    """\Wproduct:"({product_name}[^"]+)""",
    """\Wattack:"({attack}[^"]+)""",
    """\Wconfidence_level:"({confidence_level}[^"]+)""",
    """\Wrule_name:"({rule}[^"]+)""",
    """\Wrule_uid:"\{({rule_id}[^"\}]+)""",
    """\Wsmartdefense_profile:"({smartdefense_profile}[^"]+)""",
    """\Wuser:"({user}[^"\(\)]+?)\s*"""",
    """ifdir:"+({direction}[^"]+)""",
    """originsicname:"+({user_ou}[^"]+)"""
  
}
```