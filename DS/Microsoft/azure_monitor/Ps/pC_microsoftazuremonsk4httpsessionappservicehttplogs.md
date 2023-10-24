#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-http-session-appservicehttplogs
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  ParserVersion = v1.0.0
  Conditions = [
    """"resourceId":""",
    """"category":"AppServiceHTTPLogs""""
  ]
  Fields = [
    """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """([^\|]*\|){5}({operation}[^\|]+)""",
    """destinationServiceName =({app}.+?)\s+(\w+=|$)""",
    """\Wsuser=(anonymous|({email_address}[^@=]+@[^@=]+?)|({user}[\w\.\-]{1,40}\$?))(\s+[\S]+=|\s*$)""",
    """\Wsuid=(anonymous|({email_address}[^@=]+@[^@=]+?)|({user}[\w\.\-]{1,40}\$?))(\s+[\S]+=|\s*$)""",
    """"CsHost":"({app}[^:",]+)""",
    """"Result":"({action}[^"]+)"""",
    """"resourceId":"({resource}[^"]+)"""",
    """"CsUriStem":"({uri_path}[^"]+)"""",
    """"CIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"UserAgent":"(-|({user_agent}[^"]+))"""",
    """"category":"({category}[^"]+)"""",
    """"CsMethod":"({method}[^"]+)"""",
    """"SPort":"({src_port}\d+)"""",
    """"CsUriQuery":"(-|({uri_query}[^"]+))"""",
    """"CsBytes":({bytes_in}\d+),""",
    """"CsUsername":"(-|({user}[\w\.\-]{1,40}\$?))"""",
    """"Referer":"(-|({referrer}[^"]+))"""",
    """"ScBytes":({bytes_out}\d+),""",
    """"ScStatus":({http_response_code}\d+),""",
    """\[Namespace:\s*({event_hub_namespace}\S+) ; EventHub name:\s*({event_hub_name}[\w-]+)""",
    """"UserAgent":"(?:-|Mozilla\/[^"]+?({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin).+?({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident))"""
  ]
  DupFields = ["app->web_domain", "event_hub_namespace->host"]


}
```