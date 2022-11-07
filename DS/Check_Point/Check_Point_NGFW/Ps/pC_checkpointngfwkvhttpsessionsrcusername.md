#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-http-session-srcusername
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "ddMMMyyyy HH:mm:ss"
  Conditions = [ """product: URL Filtering;""", """;i/f_name:""", """;src_user_name:""" ]
  Fields = [
    """^[^;]*?({time}\d+\w{3}\d+ \d\d:\d\d:\d\d)""",
    """src_machine_name:\s*({host}[^@;]+)(@({domain}\w+))?""",
    """dst:\s+(?:-|({dest_ip}[^;]+))""",
    """service:\s+(?:-|({dest_port}\d+));""",
    """src:\s+(?:-|({src_ip}[^;]+))""",
    """s_port:\s+(?:-|({src_port}\d+));""",
    """src_user_name:\s*({last_name}[^,]+),\s*({first_name}[\w\s]+\S)\s*(\(|$)""",
    """({action}[^\s]+)\s+[^\s]+ product: """,
    """sent_bytes:\s+(?:-|({bytes_out}\d+));""",
    """received_bytes:\s+(?:-|({bytes_in}\d+))""",
    """resource:\s+(-|({url}[^;]+));\s*(\w+:|$)""",
    """resource:\s+(?:-|({protocol}[^:]+))""",
    """appi_name:\s+({web_domain}(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|[^;\/]+)""",
    """resource:\s+(?:-|(\w+:\/+[^\/]+\/({uri_path}[^?;]+)))""",
    """resource:\s+(?:-|(\w+:\/+[^?]+\?({uri_query}[^;]+)));""",
    """matched_category:\s+(?:-|({category}[^;]+))""",
    """app_properties:\s+(?:-|({category}[^,;]+));""",
  ]
  ParserVersion = "v1.0.0"


}
```