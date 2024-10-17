#### Parser Content
```Java
{
Name = "symantec-bcpa-mix-http-session-deniedtcp"
  ParserVersion = "v1.0.0"
  Conditions = [
    """ DENIED """
    """ TCP_"""
  ]
  Fields = ${BlueCoatParserTemplates.bluecoat-proxy.Fields}[
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\s\d+\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s({http_response_code}\d+)\s({proxy_action}[^\s]+)\s({bytes_out}\d+)\s({bytes_in}\d+)\s(unknown|({method}[^\s]+))\s({protocol}[^\s]+)\s(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({web_domain}[^\s]+))\s({url}[^\s]+)\s(\S+\s){2}({=dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s\S+\s"({user_agent}[^"]+)"\s({action}DENIED)\s({category}[^\s]+)""",
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\s\d+\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s({http_response_code}\d+)\s({proxy_action}[^\s]+)\s({bytes_out}\d+)\s({bytes_in}\d+)\s(unknown|({method}[^\s]+))\s({protocol}[^\s]+)\s(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({web_domain}[^\s]+))\s({dest_port}\d+)\s({uri_path}\/[^\s]*)\s(\S+\s){3}({=dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s(\S+\s){2}"({user_agent}[^"]+)"\s({action}DENIED)\s"({categories}({category}[^";]+)[^"]*)"\s""",
    """\s({action}DENIED)\s"({categories}({category}[^";]+)[^"]*)"\s\S+\s({http_response_code}\d+)\s({proxy_action}[^\s]+)\s(unknown|({method}[^\s]+))\s(-|({mime}[^\s]+))\s({protocol}[^\s]+)\s(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({web_domain}[^\s]+))\s({dest_port}\d+)\s({uri_path}\/[^\s]+)\s(\S+\s)?(-|({uri_query}\?[^\s]+))\s\S+\s"({user_agent}[^"]+)"\s({=dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s({bytes_out}\d+)\s({bytes_in}\d+)"""
    """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\dZ)\s+({host}[\w\-.]+)\s+[\w+\s+\d+]+\s+(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s+[\-\w+\d+]+\s+(-|"?[^"]*")\s+({method}[^\s]+)\s+({protocol}[^\s]+)\s+""",
    """\s+({action}OBSERVED|PROXIED|DENIED)\s+(?:-|\\?"(none|({categories}({category}[^\\";]+)[^"]*?))\\?")\s+[^\s]+\s+(?:-|({http_response_code}\d+)?)\s+(?:-|({proxy_action}[^\s]+))\s+({method}\w+)\s+([^\s]+\s+){6,8}"({user_agent}[^"]+)"\s+"""
  ]


}
```