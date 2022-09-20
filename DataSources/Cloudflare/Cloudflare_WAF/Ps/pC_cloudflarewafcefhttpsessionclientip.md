#### Parser Content
```Java
{
Name = cloudflare-waf-cef-http-session-clientip
  ParserVersion = v1.0.0
  Vendor = Cloudflare
  Product = Cloudflare WAF
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ 
"""destinationServiceName =Cloudflare"""
""""clientIP":""""
""""source":"""" 
""""clientRequestHTTPMethodName":"""" 
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s+[^\s]+\s+""",
    """"ClientDeviceType":"({device_type}[^"]+)""",
    """"clientCountryName":"({src_country}[^"]+)""",
    """"clientIP":"(?:["]+|({src_ip}[A-Fa-f:\d.]+))""",
    """"userAgent":"({user_agent}[^"]+)""",
    """"edgeResponseStatus":({edge_response_status}({http_response_code}\d\d\d))""",
    """"originResponseStatus":({origin_response_status}({http_response_code}\d\d\d))"""
    """"clientRequestHTTPMethodName":"({method}[^"]+)""",
    """"action":"({action}[^"]+)""",
    """"ClientRequestReferer":"({referrer}[^"]+?)",""",
    """"clientRequestHTTPHost":"({web_domain}[^"<,]+)""",
    """"clientRequestPath":"({uri_path}[^"]+)""",
    """"clientRequestHTTPProtocol":"({protocol}[^"//]+)""",
    ]


}
```