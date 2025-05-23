#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-http-session-ifname
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "epoch_sec"
  Conditions = [ """CheckPoint""", """product:"URL Filtering"""", """ifname:"""" ]
  Fields = [
    """\Wtime(:|=)"({time}\d{10})""",
    """\W({host}[\w\-.]+) CheckPoint""",
    """\Wuser:"({last_name}[^,]+),\s*({first_name}[\w\s]+\S)\s*\(({account}.+?)\)""",
    """\Wsrc:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst:"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
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
    """\Wuser:"(({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^"=]+?))\s*"""",
    """\W(user|src_user_name|dst_user_name):"({full_name}[^\"\(]+?)\s*\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  ]
  ParserVersion = "v1.0.0"


}
```