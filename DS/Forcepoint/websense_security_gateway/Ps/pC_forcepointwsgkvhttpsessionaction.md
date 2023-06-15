#### Parser Content
```Java
{
Name = forcepoint-wsg-kv-http-session-action
  ParserVersion = v1.0.0
  Vendor = Forcepoint
  Product = Websense Security Gateway
  TimeFormat = "yyyy:MM:dd-HH:mm:ss"
  Conditions = [
"""vendor=Websense"""
"""http_user_agent="""
"""http_proxy_status_code=""" 
]
  Fields = [
    """({host}\S+)\s+vendor=""",
    """\sdst_ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\ssrc_host=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\ssrc_port=({src_port}\d+)""",
    """\sdst_port=({dest_port}\d+)""",
    """user=[^=]+?({user_ou}\w+=[^\/]+?DC=\w+\/({full_name}[^\(]+?))\s+(\([^\)]+\)\s+)?src_host=""",
    """\saction=({action}[^\s]+)""",
    """\shttp_method=(-|({method}[^\s]+))""",
    """\sbytes_in=({bytes_in}\d+)""",
    """\sbytes_out=({bytes_out}\d+)""",
    """\surl=(?:-|({url}[^\s"]+))""",
    """\surl=(?:-|({protocol}[^:\s]+)):""",
    """\surl=([^:]+:\/+)?({web_domain}[^\s\/:]+)[^"]*?$""",
    """\surl=(?:-|\w+:\/+[^\s\/]+)\/+({uri_path}[^?\s]*)""",
    """\surl=(?:-|(?=(?)(?:[^?]+\?({uri_query}[^\s"]+))))""",
    """\shttp_user_agent=(?:-|({user_agent}[^=]+?))\s+http_proxy""",
    """\scategory=({category_id}\d+)\s+user""",
    """\shttp_content_type=(?:-|({mime}[^"]+?))\s+http_""",
    """\shttp_proxy_status_code=({http_response_code}\d+)""",
    """\sdisposition=({disposition}[^=]+?)\s+(\w+=|$)""",
    """\sreason=(-|({result_reason}[^=]+?))\s+(\w+=|$)"""
  ]


}
```