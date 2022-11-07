#### Parser Content
```Java
{
Name = sigsci-sigsci-json-http-session-uri
  ParserVersion = "v1.0.0"
  Vendor = SIGSCI
  Product = SIGSCI
  TimeFormat ="yyyy-MM-dd'T'HH:ss:SSZ"
  Conditions = [ 
"""serverHostname"""
"""remoteHostname"""
"""serverName"""
"""uri"""
]
  Fields = [
    """"+serverHostname"+:"+({src_host}[^"]+)""",
    """"+remoteIP"+:"+({dest_ip}[^"]+)""",
    """"+remoteHostname"+:"+(|({dest_host}[^"\s,]+))"""",
    """"userAgent":"(|({user_agent}[^"]+))"""",
    """"+timestamp"+:"+({time}[^"]+)""",
    """"+method"+:"+({method}[^"]+)""",
    """"+path"+:"+({uri_path}[^"]+)""",
    """"+responseCode"+:({http_response_code}\d+)""",
    """"+(H|h)ost"+."+({host}[^"\]]+?)(:\d+)?"""",
    """BLOCKED"*":\s*\{"+type"+:"+({action}[^"]+)""",
    """"+protocol"+:"+({protocol}\w+\/[^"]+)""",
    """"+Content-Type"+(:|,)"+({mime}[^";]+)""",
    """"+responseSize"+:({bytes_out}\d+)"""
    ]


}
```