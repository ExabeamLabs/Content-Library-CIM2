#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-http-session-success-allow
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "epoch_sec"
  Conditions = [ """CheckPoint""", """product:""", """action:\"Allow\"""" ]
  Fields = [
    """\Wtime:\\"({time}\d+)""",
    """\W({host}[\w\-.]+) CheckPoint""",
    """\Wsrc:\\"({src_ip}[A-Fa-f:\d.]+)""",
    """\Wdst:\\"(0\.0\.0\.0|({dest_ip}[A-Fa-f:\d.]+))""",
    """\Waction:\\"({action}[^"\\]+)""",
    """\Ws_port:\\"({src_port}\d+)""",
    """\Wifdir:\\"({direction}[^"\\]+)""",
    """\Worigin:\\"({origin_ip}[^"\\]+)""",
    """\Worigin_?sic_?name:\\"CN=({origin_name}[^",\\]+)""",
    """product:\\"({product_name}[^"\\]+)""",
    """\Wservice:\\"({dest_port}\d+)""",
    """\Wproto:\\"({protocol}[^"\\]+)""",
    """\Wapp_rule_id:\\"\{({rule_id}[^"\}\\]+)""",
    """\Wifname:\\"({interface_name}[^"\\]+)""",
    """\Wweb_client_type:\\"Other:\s*({user_agent}[^"\\]+)""",
  ]
  DupFields = [ "action->event_name" ]
  ParserVersion = "v1.0.0"


}
```