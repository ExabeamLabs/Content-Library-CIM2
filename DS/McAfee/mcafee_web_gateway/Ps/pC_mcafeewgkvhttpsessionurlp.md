#### Parser Content
```Java
{
Name = mcafee-wg-kv-http-session-urlp
  ParserVersion = v1.0.0
  Vendor = McAfee
  Product = McAfee Web Gateway
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """mwg: status="""", """srcip="""", """mtd="""", """urlp="""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+mwg:""",
    """\Wstatus="({http_response_code}\d+)""",
    """\Wsrcip="(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
    """\Wuser="(-|({user}[^"]+))"""",
    """\Wdst_ip="(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""",
    """\Wurlp="(-|({dest_port}\d+))""",
    """\Wproto="(-|({protocol}[^"]+))"""",
    """\Wmtd="(-|({method}[^"]+))"""",
    """\Wurlc="(-|({category}[^"]+))"""",
    """\Wmt="(-|({mime}[^"]+))"""",
    """\Wbytes="(-|({bytes_in}\d+)\/({bytes_out}\d+)\/({bytes_in_post}\d+)\/({bytes_in_get}\d+))"""",
    """\Wua="(-|({user_agent}[^"]+))"""",
    """\Wrule="(-|({proxy_action}[^"]+))"""",
    """\Wurl="(-|({url}[^"]+))"""",
    """\Wurl="(?:[^:]+:\/+)({web_domain}[^\/:\s]+)""",
    """\Wurl="(?:-|\w+:\/+[^\/]+)({uri_path}\/[^?\s]+)""",
    """\Wurl="(-|([^?]+({uri_query}\?[^\s"]+)))""",
  ]


}
```