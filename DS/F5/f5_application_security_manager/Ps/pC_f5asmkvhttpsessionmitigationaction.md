#### Parser Content
```Java
{
Name = "f5-asm-kv-http-session-mitigationaction"
Vendor = "F5"
Product = "F5 Application Security Manager"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
""",device_vendor="F5""""
""",client_ip="""
""",client_port="""
""",http_method=""""
""",configured_mitigation_action="""
]
  Fields = [
    """,request_date_time="({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)"""",
    """hostname="({host}[\w\-.]+)"""",
    """,host="({web_domain}[^:"]+)""",
    """,client_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """,client_port="({src_port}\d+)"""",
    """,dest_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """dest_port="({dest_port}\d+)"""",
    """http_method="({method}[^"]+)"""",
    """http_protocol_indication="({protocol}[^"]+)"""",
    """configured_mitigation_action="(None|({result}[^"]+))"""",
    """((?i)User-Agent):\s*({user_agent}[^"]+?)[\\r\\n]+([\w-]+:|")""",
    """http_request="(\w+\s)?({uri_path}\/[^"\s?]+?)(\?({uri_query}[^\s]+))?\s"""
  ]

ParserVersion = "v1.0.0"


}
```