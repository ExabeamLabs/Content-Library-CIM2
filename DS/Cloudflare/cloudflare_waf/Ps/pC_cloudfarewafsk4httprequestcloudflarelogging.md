#### Parser Content
```Java
{
Name = cloudfare-waf-sk4-http-request-cloudflarelogging
  ParserVersion = v1.0.0
  Vendor = Cloudflare
  Product = Cloudflare WAF
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """requestClientApplication=CloudflareLogging""", """"EdgeStartTimestamp":"""", """CEF""" ]
  Fields = [
    """"EdgeStartTimestamp":"({time}[^"]+)"""
    """"ClientDeviceType":"({device_type}[^"]+)"""
    """"ClientCountry":"({src_country}[^"]+)"""
    """"ClientIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"ClientRequestUserAgent":"({user_agent}[^"]+)"""
    """"ClientRequestURI":"({request_uri}[^"]+)"""
    """"EdgeResponseStatus":({edge_response_status}({http_response_code}\d\d\d))"""
    """"OriginResponseStatus":({origin_response_status}({http_response_code}\d\d\d))"""
    """"OriginIP":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
# ray_id is removed
# worker_subrequest is removed
    """"ClientRequestMethod":"({method}[^"]+)"""
  ]


}
```