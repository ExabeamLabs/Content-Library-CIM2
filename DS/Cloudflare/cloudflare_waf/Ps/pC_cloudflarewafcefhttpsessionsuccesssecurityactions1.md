#### Parser Content
```Java
{
Name = cloudflare-waf-cef-http-session-success-securityactions-1
  Vendor = Cloudflare
  Product = Cloudflare WAF
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """destinationServiceName =Cloudflare""", """"ClientIP":"""", """"SecurityActions":""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)\s+[^\s]+\s+""",
    """"ClientRequestHost":"({host}[^"]+)""",
    """"RayID":"({alert_id}[^"]+)""",
    """"SecurityAction":"(unknown|({proxy_action}[^"]+))""",
    """"SecurityRuleID":"({event_code}[^"]+)""",
    """"SecurityRuleDescription":"({additional_info}[^"]+)""",
    """dhost=({dest_host}[^\s]+)""",
    """suser=(anonymous|({user}[\w\.\-]{1,40}\$?))""",
    """"ClientDeviceType":"({device_type}[^"]+)""",
    """"ClientCountry":"({src_country}[^"]+)""",
    """"ClientIP":"(?:["]+|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """"ClientSrcPort":({src_port}\d+)""",
    """"ClientRequestUserAgent":"({user_agent}[^"]+)""",
    """"ClientRequestBytes":({bytes_in}\d+)""",
    """"EdgeResponseBytes":({bytes_out}\d+)""",
    """"edgeResponseStatus":({edge_response_status}({http_response_code}\d\d\d))""",
    """"originResponseStatus":({origin_response_status}({http_response_code}\d\d\d))"""
    """"EdgeServerIP":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """"OriginIP":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"*[^=]+?OriginResponseBytes":({bytes_out}\d+)""",
    """"OriginIP":"(?:["]+|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))""",
    """"ClientRequestMethod":"(UNKNOWN|({method}[^"]+))""",
    """"SecurityActions[":\[]+(?:["\]]+|({action}[^,"]+))""",
    """\|act=({action}[^\s]+)\s\w+=""",
    """"ClientRequestHost":"({web_domain}[^"]+)""",
    """"ClientRequestURI":"({uri_path}[^"\?\s]+)(?:\?({uri_query}[^?\s"]+))?""",
    """"ClientRequestProtocol":"({protocol}[^"]+)""",
    """"SecurityLevel":"({alert_severity}[^"]+)""",
    """"ClientRequestReferer":"({referrer}[^"]+?)",""",
    ]


}
```