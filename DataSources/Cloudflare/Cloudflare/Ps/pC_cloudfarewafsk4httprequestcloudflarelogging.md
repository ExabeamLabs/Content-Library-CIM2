#### Parser Content
```Java
{
Name = cloudfare-waf-sk4-http-request-cloudflarelogging
  ParserVersion = v1.0.0
  Vendor = Cloudflare
  Product = Cloudflare
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """requestClientApplication=CloudflareLogging""", """"EdgeStartTimestamp":"""", """CEF""" ]
  Fields = [
    """"EdgeStartTimestamp":"({time}[^"]+)"""
    """"ClientDeviceType":"({device_type}[^"]+)"""
    """"ClientCountry":"({src_country}[^"]+)"""
    """"ClientIP":"({src_ip}[A-Fa-f:\d.]+)""""
    """"ClientRequestUserAgent":"({user_agent}[^"]+)"""
    """"ClientRequestURI":"({request_uri}[^"]+)"""
    """"EdgeResponseStatus":({edge_response_status}({http_response_code}\d\d\d))"""
    """"OriginResponseStatus":({origin_response_status}({http_response_code}\d\d\d))"""
    """"OriginIP":"({dest_ip}[A-Fa-f:\d.]+)""""
# ray_id is removed
# worker_subrequest is removed
    """"ClientRequestMethod":"({method}[^"]+)"""
  ]


}
```