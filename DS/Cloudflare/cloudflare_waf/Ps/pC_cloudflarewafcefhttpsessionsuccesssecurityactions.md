#### Parser Content
```Java
{
Name = cloudflare-waf-cef-http-session-success-securityactions
  Vendor = Cloudflare
  Product = Cloudflare WAF
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """destinationServiceName =Cloudflare""", """ResponseStatus"""", """SecurityActions""", """"ClientRequestMethod":""" ]
  Fields = [
    """"EdgeStartTimestamp"+:"*({time}\d+)""",
    """"EdgeStartTimestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"ClientDeviceType"+:"+({device_type}[^"]+)""",
    """"ClientCountry"+:"+({src_country}[^"]+)""",
    """"clientIp"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """"ClientSrcPort"+:({src_port}\d+)""",
    """"ClientRequestUserAgent"+:"+({user_agent}[^"]+)""",
    """"ClientRequestBytes"+:({bytes_in}\d+)""",
    """"EdgeResponseBytes"+:({bytes_out}\d+)""",
    """"edgeResponseStatus":({edge_response_status}({http_response_code}\d\d\d))""",
    """"originResponseStatus":({origin_response_status}({http_response_code}\d\d\d))"""
    """"EdgeServerIP"+:"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """"OriginIP"+:"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"*.*OriginResponseBytes"+:({bytes_out}\d+)""",
    """"OriginIP"+:"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """"ClientRequestMethod"+:"+({method}[^"]+)""",
    """"SecurityActions[":\[]+(?:["\]]+|({action}[^,"]+))""",
    """"ClientRequestHost"+:"+({web_domain}[^"]+)""",
    """"ClientRequestURI"+:"+({uri_query}[^"\s]+)""",
    """"ClientRequestPath"+:"+({uri_path}[^"]+)""",
    """"ClientRequestProtocol"+:"+({protocol}[^"]+)""",
    """"SecurityLevel"+:"+({alert_severity}[^"]+)"""
  ]
  DupFields = [ "dest_ip->host" ]


}
```