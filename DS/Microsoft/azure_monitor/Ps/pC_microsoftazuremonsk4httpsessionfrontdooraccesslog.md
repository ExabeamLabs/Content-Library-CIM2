#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-http-session-frontdooraccesslog
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  ParserVersion = v1.0.0
  Conditions = [
    """"resourceId"""",
    """"category":"FrontdoorAccessLog"""",
    """"httpMethod":""""
  ]
  Fields = [
   """"time":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)"""",
   """"backendHostname":"({host}[^:"]+)""",
   """"httpMethod":"({method}[^"]+)"""",
   """"requestUri":"({url}[^:\\\/\s,"]+:[\\\/]+[^\/]+(\/|({uri_path}\/[^\?"\s]*))?({uri_query}\?[^"\s]*)?)""""
   """"requestUri":".*?({web_domain}[^\/\.\s]+(?i)(\.(com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ai|ms|mx|))+)[\\\/\s:"]""",
   """"clientIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
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
   """suser=(anonymous|({user}[\w\.\-]{1,40}\$?))\s+\w+=""",
   """"resourceId":"({object}[^"]+)""",
   """"operationName":"({operation}[^"]+)""",
   """destinationServiceName =({app}[^=]+)\s+(\w+=|$)"""
  ]
   DupFields=["event_hub_namespace->host", "object->resource"]


}
```