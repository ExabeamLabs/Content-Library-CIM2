#### Parser Content
```Java
{
Name = cloudflare-waf-cef-http-session-clientip
  ParserVersion = v1.0.0
  Vendor = Cloudflare
  Product = Cloudflare WAF
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ 
""""edgeResponseStatus":"""
""""clientIP":""""
""""source":"""" 
""""clientRequestHTTPMethodName":"""" 
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s+[^\s]+\s+""",
    """"ClientDeviceType":"({device_type}[^"]+)""",
    """"clientCountryName":"({src_country}[^"]+)""",
    """"clientIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"userAgent":"({user_agent}[^"]+)""",
    """"edgeResponseStatus":({edge_response_status}({http_response_code}\d\d\d))""",
    """"originResponseStatus":({origin_response_status}({http_response_code}\d\d\d))"""
    """"clientRequestHTTPMethodName":"({method}[^"]+)""",
    """"action":"({action}[^"]+)""",
    """"ClientRequestReferer":"({referrer}[^"]+?)",""",
    """"clientRequestHTTPHost":"({web_domain}[^"<,]+)""",
    """"clientRequestPath":"({uri_path}[^"]+)""",
    """"clientRequestHTTPProtocol":"({protocol}[^"\/]+)""",
    ]


}
```