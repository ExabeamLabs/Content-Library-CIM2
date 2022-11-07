#### Parser Content
```Java
{
Name = cloudflare-waf-sk4-http-session-firewallmatchesactions
  ParserVersion = v1.0.0
  Vendor = Cloudflare
  Product = Cloudflare WAF
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """destinationServiceName =Cloudflare""", """ResponseStatus"""", """FirewallMatchesActions""" ]
  Fields = [
    """"EdgeStartTimestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"ClientDeviceType":"({device_type}[^"]+)""",
    """"ClientCountry":"({src_country}[^"]+)""",
    """"ClientIP":"(?:["]+|({src_ip}[A-Fa-f:\d.]+))""",
    """"ClientSrcPort":({src_port}\d+)""",
    """"ClientRequestUserAgent":"({user_agent}[^"]+)""",
    """"ClientRequestBytes":({bytes_in}\d+)""",
    """"EdgeResponseBytes":({bytes_out}\d+)""",
    """"EdgeResponseStatus":({edge_response_status}({http_response_code}\d\d\d))"""
    """"OriginResponseStatus":({origin_response_status}({http_response_code}\d\d\d))"""
    """"EdgeServerIP":"({dest_ip}[A-Fa-f:\d.]+)""",
    """"OriginIP":"({dest_ip}[A-Fa-f:\d.]+)"*.*OriginResponseBytes":({bytes_out}\d+)""",
    """"OriginIP":"(?:["]+|({dest_ip}[A-Fa-f:\d.]+))""",
    """"ClientRequestMethod":"({method}[^"]+)""",
    """"FirewallMatchesActions[":\[]+(?:["\]]+|({action}[^,"]+))""",
    """"ClientRequestHost":"({web_domain}[^"]+)""",
    """"ClientRequestURI":"({uri_query}[^"\s]+)""",
    """"ClientRequestPath":"({uri_path}[^"]+)""",
    """"ClientRequestProtocol":"({protocol}[^"]+)""",
    """"SecurityLevel"+:"+({alert_severity}[^"]+)"""
  ]
  DupFields = [ "dest_ip->host" ]


}
```