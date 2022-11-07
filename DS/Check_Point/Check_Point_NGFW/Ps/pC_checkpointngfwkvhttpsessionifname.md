#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-http-session-ifname
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "epoch_sec"
  Conditions = [ """CheckPoint""", """product:"URL Filtering"""", """ifname:"""" ]
  Fields = [
    """\Wtime:"({time}\d+)""",
    """\W({host}[\w\-.]+) CheckPoint""",
    """\Wuser:"({last_name}[^,]+),\s*({first_name}[\w\s]+\S)\s*\(({account}.+?)\)""",
    """\Wsrc:"({src_ip}[A-Fa-f:\d.]+)""",
    """\Wdst:"({dest_ip}[A-Fa-f:\d.]+)""",
    """\Waction:"({action}[^"]+)""",
    """\Ws_port:"({src_port}\d+)""",
    """\Wproto:"({protocol}[^"]+)""",
    """\Wservice:"({dest_port}\d+)""",
    """\Wmatched_category:"({category}[^"]+)""",
    """\Wappi_name:"\s*({web_domain}(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|[^;\/"]+)""",
    """\Wresource:"\s*(-|({url}[^"]+))""",
    """\Wresource:"\s*(?:-|({protocol}[^:]+))""",
    """\Wresource:"\s*(?:-|(\w+:\/+[^\/]+\/({uri_path}[^?;"]+)))""",
    """\Wresource:"\s*(?:-|(\w+:\/+[^?]+({uri_query}\?[^;"]+?)))"""",
    """\Wweb_client_type:"(Other:)?\s*(?:-|({user_agent}[^"]+))""",
    """\Worigin:"({origin_ip}[^"]+)""",
    """\Worigin_sic_name:"CN=({origin_name}[^",]+)""",
    """\Wproduct:"({product_name}[^"]+)""",
    """\Wsrc_machine_name:"({src_host}[^"@]+)@({domain}[^"]+)""",
    """\Wuser:"({user}[^"]+?)\s*"""",
  ]
  ParserVersion = "v1.0.0"


}
```