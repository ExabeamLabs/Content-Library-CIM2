#### Parser Content
```Java
{
Name = cloudflare-waf-cef-http-session-firewall
  ParserVersion = v1.0.0
  Vendor = Cloudflare
  Product = Cloudflare WAF
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ 
"""destinationServiceName =Cloudflare""" 
""""ClientIP":""""
""""FirewallMatchesActions":""" 
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s+[^\s]+\s+""",
    """"ClientRequestHost":"({host}[^"]+)""",
    """"RayID":"({alert_id}[^"]+)""",
    """"WAFAction":"(unknown|({proxy_action}[^"]+))""",
    """"WAFRuleID":"({event_code}[^"]+)""",
    """"WAFRuleMessage":"({additional_info}[^"]+)""",
    """dhost=({dest_host}[^\s]+)""",
    """suser=(anonymous|({user}[^\s]+))""",
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
    """"OriginIP":"({dest_ip}[A-Fa-f:\d.]+)"*[^=]+?OriginResponseBytes":({bytes_out}\d+)""",
    """"OriginIP":"(?:["]+|({dest_ip}[A-Fa-f:\d.]+))""",
    """"ClientRequestMethod":"(UNKNOWN|({method}[^"]+))""",
    """"FirewallMatchesActions[":\[]+(?:["\]]+|({action}[^,"]+))""",
    """\|act=({action}[^\s]+)\s\w+=""",
    """"ClientRequestHost":"({web_domain}[^"]+)""",
    """"ClientRequestURI":"({uri_path}[^"\?\s]+)(?:\?({uri_query}[^?\s"]+))?""",
    """"ClientRequestProtocol":"({protocol}[^"]+)""",
    """"SecurityLevel":"({alert_severity}[^"]+)""",
    """"ClientRequestReferer":"({referrer}[^"]+?)",""",
    ]


}
```