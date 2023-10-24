#### Parser Content
```Java
{
Name = cloudflare-waf-json-http-session-firewall
  ParserVersion = v1.0.0
  Vendor = Cloudflare
  Product = Cloudflare WAF
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [  """ClientRequestUserAgent""", """"ClientIPClass":"""", """"ClientASN":""", """"ClientCountry":"""", """"ClientIP":"""", """"RayID":"""", """"EdgeColoCode":"""" ]
  Fields = [
    """"ClientRequestHost":"({host}[^"]+)""",
    """"RayID":"({alert_id}[^"]+)""",
    """"ClientCountry":"({src_country}[^"]+)""",
    """"ClientIP":"(?:["]+|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """"ClientSrcPort":({src_port}\d+)""",
    """"ClientRequestUserAgent":"({user_agent}[^"]+)""",
    """"EdgeResponseStatus":({edge_response_status}({http_response_code}\d\d\d))"""
    """"OriginResponseStatus":({origin_response_status}({http_response_code}\d\d\d))"""
    """"ClientRequestMethod":"(UNKNOWN|({method}[^"]+))""",
    """"ClientRequestHost":"({web_domain}[^"]+)""",
    """"ClientRequestProtocol":"({protocol}[^"]+)""",
    
    ]



}
```