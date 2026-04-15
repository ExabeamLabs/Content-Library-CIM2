#### Parser Content
```Java
{
Name = "symantec-bcpa-mix-http-session-connect"
  ParserVersion = "v1.0.0"
  Conditions = [ """ CONNECT """, """ TCP_""", """ tcp """ ]
  Fields = ${BlueCoatParserTemplates.bluecoat-proxy.Fields}[
    """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\dZ)\s+({host}[\w\-.]+)\s+[\w+\s+\d+]+\s+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s+[\-\w+\d+]+\s+(-|"?[^"]*")\s+({method}[^\s]+)\s+({protocol}[^\s]+)\s+""",
    """\s+({action}OBSERVED|PROXIED|DENIED)\s+"*({category}[^"]+)"*\s*(?:-|\\?"(none|({categories}[^\\";]+[^"]*?))\\?")\s+(?:-|({proxy_action}[^\s]+))\s+(?:-|({referrer}[^\s]+))\s+(?:-|({http_response_code}\d+)?)\s+[^"]+"({method}[^"]+)"(\s+[\w\-\.\/]+){6}(\s+|")({user_agent}[^\%\s]+)\s*""",
    """({host}[\w\-\.]+)\s\d\d\d\d\-\d\d-\d\d\s\d\d:\d\d:\d\d\s(\d+\s)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s(-|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s(\S+\s*){6}"""
    """({action}OBSERVED|PROXIED|DENIED)\s"({categories}({category}[^",]+)[^"]*)"\s((-|({referrer}\S+))\s+)?({http_response_code}\0|\d{3})\s({proxy_action}[^\s]+)\s({method}[^\s]+)\s\S\s({protocol}[^\s]+)\s({web_domain}[^\s]+)\s({dest_port}\d+)\s(-|({uri_path}\/[^\s]*))\s(-|({uri_query}\?[^\s]+))\s\S+\s(-|"({user_agent}[^"]+)")\s(\d{1,3}\.){3}\d{1,3}\s({bytes_out}\d+)\s({bytes_in}\d+)"""
  ]


}
```