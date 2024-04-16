#### Parser Content
```Java
{
Name = "f5-websafe-str-http-session-cookiemonster"
  Vendor = F5
  Product = F5 WebSafe
  TimeFormat = "dd/MM/yyyy HH:mm:ss Z"
  Conditions = [ """cookiemonster=""" ]
  Fields = [
    """({host}[\w\-.]+)\s\S+\s({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d [-+]\d+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s(-|({user}[\w\.\-]{1,40}\$?))\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+.+?({http_response_code}\d+)\s\d+\s\d+\s\S+\s"({user_agent}[^"]+)""",
    """cookiemonster=.+?(\}|\=\=)\s+({url}.+?)\s*$""",
    """cookiemonster=.+?(\}|\=\=)\s+(?:-|({protocol}[^:]+))""",
    """cookiemonster=.+?(\}|\=\=)\s+(?:[^:]+:\/+)({web_domain}[^\/:\s]+)""",
    """cookiemonster=.+?(\}|\=\=)\s+(?:-|\w+:\/+[^\/]+)({uri_path}\/[^?\s]+)""",
    """cookiemonster=.+?(\}|\=\=)\s+(?:-|(?=(?)(?:[^?]+({uri_query}\?[^\s"]+))))""",
    """cookiemonster=.+?(\}|\=\=)\s+.+?METHOD=({method}\w+)""",
  ]
  ParserVersion = "v1.0.0"


}
```