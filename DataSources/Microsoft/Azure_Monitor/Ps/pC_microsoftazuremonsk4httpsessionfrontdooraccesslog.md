#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-http-session-frontdooraccesslog
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  ParserVersion = v1.0.0
  Conditions = [
    """destinationServiceName =Azure""",
    """"category":"FrontdoorAccessLog"""",
    """"httpMethod":""""
  ]
  Fields = [
   """"time":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)"""",
   """"backendHostname":"({host}[^:"]+)""",
   """"httpMethod":"({method}[^"]+)"""",
   """"requestUri":"({url}[^:\\\/\s,"]+:[\\\/]+[^\/]+(\/|({uri_path}\/[^\?"\s]*))?({uri_query}\?[^"\s]*)?)""""
   """"requestUri":".*?({web_domain}[^\/\.\s]+(?i)(\.(com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ai|ms|mx|))+)[\\\/\s:"]""",
   """"clientIp":"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""",
   """"clientPort":"({src_port}\d+)"""",
   """"httpStatusCode":"({http_response_code}\d+)""",
   """"requestBytes":"({bytes_in}\d+)"""",
   """"responseBytes":"({bytes_out}\d+)"""",
   """"userAgent":"({user_agent}[^"]+)"""",
   """"securityProtocol":"({protocol}[^\s"]+)""",
   """"userAgent":"(?:-|Mozilla\/.+\(({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin).+?([uU]nknown|({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident)))"""
   """Namespace:\s*({event_hub_namespace}\S+)""",
   """EventHub name:\s*({event_hub_name}.+?)\s*\]""",
   """"category":"({category}[^"]+)""",
   """suser=(anonymous|({user}.+?))\s+\w+=""",
   """"resourceId":"({object}[^"]+)""",
  ]
   DupFields=["event_hub_namespace->host"]


}
```