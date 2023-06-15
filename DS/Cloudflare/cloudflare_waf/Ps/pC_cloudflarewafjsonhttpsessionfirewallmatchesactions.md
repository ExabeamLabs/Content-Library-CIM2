#### Parser Content
```Java
{
Name = cloudflare-waf-json-http-session-firewallmatchesactions
  Vendor = Cloudflare
  Product = Cloudflare WAF
  TimeFormat = "epoch"
  Conditions = [ """"WAFAction":"""", """ResponseStatus"""", """FirewallMatchesActions""", """"ZoneName":"""" ]
  Fields = [
    """"EdgeStartTimestamp":({time}\d{13})""",
    """"ClientDeviceType":"({device_type}[^"]+)"""",
    """"ClientCountry":"({src_country}[^"]+)"""",
    """"ClientIP":"(?:["]+|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
    """"ClientSrcPort":({src_port}\d+)""",
    """"ClientRequestUserAgent":"({user_agent}[^"]+)"""",
    """"ClientRequestBytes":({bytes_in}\d+)""",
    """"EdgeResponseBytes":({bytes_out}\d+)""",
    """"EdgeResponseStatus":({edge_response_status}({http_response_code}\d\d\d))"""
    """"OriginResponseStatus":({origin_response_status}({http_response_code}\d\d\d))"""
    """"EdgeServerIP":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"OriginIP":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"*[^=]+?OriginResponseBytes":({bytes_out}\d+)""",
    """"OriginIP":"(?:["]+|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""",
    """"ClientRequestMethod":"({method}[^"]+)"""",
    """"FirewallMatchesActions[":\[]+(?:["\]]+|({action}[^,"]+))"""",
    """"ClientRequestHost":"({web_domain}[^"]+?)(:\d+)?"""",
    """"ClientRequestURI":"({uri_path}[^"\?\s]+)(?:\?({uri_query}[^?\s"]+))?""",
    """"ClientRequestProtocol":"({protocol}[^"]+)"""",
    """"ClientRequestReferer":"({referrer}[^"]+?)",""",
    """"EdgeResponseContentType":"({mime}[^"]+)"""",
    """"SecurityLevel"+:"+({alert_severity}[^"]+)"""",
    """"RayID":"({alert_id}[^"]+)""",
    """"WAFAction":"(unknown|({proxy_action}[^"]+))""",
    """"WAFRuleID":"({event_code}[^"]+)""",
    """"WAFRuleMessage":"({additional_info}[^"]+)"""
  ]
  ParserVersion = v1.0.0


}
```