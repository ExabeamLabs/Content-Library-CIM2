#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-http-session-user
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "ddMMMyyyy HH:mm:ss"
  Conditions = [ """product: URL Filtering;""", """;i/f_name:""", """;user:""" ]
  Fields = [
    """\s({time}\d+\w{3}\d+ \d\d:\d\d:\d\d)""",
    """dst:\s+(?:-|({dest_ip}[^;]+))""",
    """service:\s+(?:-|({dest_port}\d+));""",
    """src:\s+(?:-|({src_ip}[^;]+))""",
    """s_port:\s+(?:-|({src_port}\d+));""",
    """user:.+?\(({user}[^)]+)\)\s+;web_client_type:""",
    """({action}[^\s]+)\s+[^\s]+ product: """,
    """sent_bytes:\s+(?:-|({bytes_out}\d+));""",
    """received_bytes:\s+(?:-|({bytes_in}\d+))""",
    """resource:\s+(-|({url}[^;]+));\s*(\w+:|$)""",
    """resource:\s+(?:-|({protocol}[^:]+))""",
    """appi_name:\s+({web_domain}(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|[^;\/]+)""",
    """resource:\s+(?:-|(\w+:\/+[^\/]+\/({uri_path}[^?;]+)))""",
    """resource:\s+(?:-|(\w+:\/+[^?]+({uri_query}[^;]+)));sent_bytes:""",
    """web_client_type:\s+(?:-|({user_agent}[^;]+))""",
    """matched_category:\s+(?:-|({category}[^;]+))""",
    """app_properties:\s+(?:-|({category}[^,;]+)).*matched_category:\s+High Risk""",
  ]
  ParserVersion = "v1.0.0"


}
```