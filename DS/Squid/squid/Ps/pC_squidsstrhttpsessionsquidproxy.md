#### Parser Content
```Java
{
Name = squid-s-str-http-session-squidproxy
  Vendor = Squid
  Product = Squid
  ParserVersion = "v1.0.0"
  TimeFormat = "dd/MMM/yyyy:HH:mm:ss z"
  Conditions = [ """] SquidProxy """ ]
  Fields = [
    """(-|({host}[a-fA-F\d:\.]+))\s\S+\s\S+\s\[({time}\d\d\/\w{3}\/\d\d\d\d:\d\d:\d\d:\d\d\s[+-]\d{4})\]\sSquidProxy""",
    """SquidProxy\s\S+\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """SquidProxy\s(\S+\s){2}"({method}[^\s]+)\s""",
    """SquidProxy\s(\S+\s){2}"\S+\s\S+\s({protocol}[^"\/]+)""",
    """SquidProxy\s(\S+\s){2}"[^"]+"\s({http_response_code}\d{1,3})\s""",
    """SquidProxy\s(\S+\s){2}"[^"]+"\s\d{1,3}\s({bytes}\d{1,20})\s(NONE_NONE|({proxy_action}[^:]+)):""",
    """SquidProxy\s(\S+\s){2}"\S+\s(http:\/\/)?({web_domain}[^\s\/"]+?)?(:({dest_port}\d{1,5}))?({uri_path}\/[^"\s\?]*)?({uri_query}\?[^"\s]+)?\s"""
  ]


}
```