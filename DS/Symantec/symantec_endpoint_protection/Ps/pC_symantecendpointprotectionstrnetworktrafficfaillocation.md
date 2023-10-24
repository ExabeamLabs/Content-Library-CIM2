#### Parser Content
```Java
{
Name = symantec-endpointprotection-str-network-traffic-fail-location
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
""",User Name: """,
""",Action: """,
""",Domain Name: """,
""",Rule: """,
""",Location: """
  ]
  Fields = [
    """({direction}Inbound|Outbound),Begin:\s+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\+\d+:\d+,\s+({host}[^,]+)""",
    """Local Host IP:\s+(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """Local Port:\s+({src_port}\d+)""",
    """Local Host MAC:\s+({src_mac}[^,\s]+)""",
    """Remote Host IP:\s+(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """Remote Host Name:\s+({dest_host}[^,\s]+)""",
    """Remote Port:\s+({dest_port}\d+)""",
    """Remote Host MAC:\s+({dest_mac}[^,\s]+)""",
    """User Name:\s+(SYSTEM|none|NETWORK|LOCAL|({user}[\w\.\-]{1,40}\$?))""",
    """Application:\s+({process_path}({process_dir}[^,]*?[\\\/]+)({process_name}[^,\\\/]+)),"""
    """Rule:\s+(?:|({rule}[^,]+)),""",
    """Domain Name:\s+({domain}[^\s,]+)""",
    """Action:\s+({action}[^\s,]+)""",
    """SHA-256:\s+({hash_sha256}[^\s,]+)""",
    """MD-5:\s+({hash_md5}[^\s,]+)""",
  ]


}
```