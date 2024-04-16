#### Parser Content
```Java
{
Name = "f5-bigip-kv-http-traffic-success-method"
ParserVersion = "v1.0.0"
Vendor = "F5"
Product = "F5 BIG-IP"
TimeFormat = ["MMM  d HH:mm:ss","MMM dd HH:mm:ss"]
Conditions = [
"""f5_irule"""
"""src_ip="""
"""vip_ip="""
"""http_method="""
]
  Fields = [
    """({time}\w+\s+\d+\s+\d\d:\d\d:\d\d)\s+({host}[\w\-\.]+) tmm""",
    """src_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """src_port=({src_port}\d+)""",
    """http_uri=({uri_path}[^,=\?]+)(\?({uri_query}[^=,]+))?""",
    """http_method=({method}[^,]+),""",
    """http_user_agent=({user_agent}[^,]+),"""
    """http_content_type=({mime}[^,]+)"""
  ]


}
```