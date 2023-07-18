#### Parser Content
```Java
{
Name = symantec-endpointprotection-kv-network-traffic-fail-rule
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""SymantecServer""",
"""User Name: """,
"""Rule: """
  ]
  Fields = [
    """\d\d:\d\d:\d\d (({host}[\w-]+)\s+)?SymantecServer: (({=host}[\w-]+),)?({src_host}[^,]+),Local Host IP:"""
    """Local Host IP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Local Port:\s*({src_port}\d+)""",
    """Local Host MAC:\s*({src_mac}[^,\s]+)""",
    """Remote Host IP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """Remote Host Name:\s*({dest_host}[^,\s]+)""",
    """Remote Port:\s*({dest_port}\d+)""",
    """Remote Host MAC:\s*({dest_mac}[^,\s]+)""",
    """({protocol}[^,\s]+),({direction}Inbound|Outbound)""",
    """Begin:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """,\s*Application:\s*({process_path}({process_dir}[^,]*?[\\\/]+)({process_name}[^,\\\/]+)),"""
    """User Name:\s*(SYSTEM|none|NETWORK|LOCAL|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)))""",
    """Rule:\s+(?:|({rule}[^,]+)),""",
    """Domain Name:\s+({domain}[^,]+)""",
    """Action:\s*({action}[^\s,]+)""",
    """SHA-256:\s*({hash_sha256}[^\s,]+)""",
    """MD-5:\s*({hash_md5}[^\s,]+)""",
  ]


}
```