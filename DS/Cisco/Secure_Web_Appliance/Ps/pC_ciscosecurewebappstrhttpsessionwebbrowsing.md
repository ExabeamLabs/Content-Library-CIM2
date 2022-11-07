#### Parser Content
```Java
{
Name = cisco-securewebapp-str-http-session-webbrowsing
    Vendor = Cisco
    Product = Secure Web Appliance
    TimeFormat = "epoch_sec"
    Conditions = [ """cisco:webbrowsing"""]
    Fields = [
                """({time}\d{10})\.\d{3}""",
                """\d{10}\.\d{3}\s+[^\s]+\s(?:-|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))\s([^\s]+\s){2}(?:-|"(({domain}[^\\]+)\\+)?({user}[^@"]+)[^"]*")\s(?:-|({bytes_out}\d+))\s(?:-|({bytes_in}\d+))\s(?:-|({http_response_code}\d+))\s(?:-|({proxy_action}[^\s]+))\s(?:-|({method}[^\s]+))\s(?:-|(({protocol}[^:]+):\/+)?({url}({web_domain}(?:(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|[^\s\/:]+))(:({dest_port}\d+))?(?:-|({uri_path}\/[^?\s]*))?({uri_query}\?[^\s]+)?))\s(("[^"]+")|[^\s]+)\s+[^\s]+\s(?:-|({dest_ip}[^\s]+))\s([^\s]+\s){2}(?:-|"({category}[^"]+)")\s[^\s]+\s(?:-|({mime}[^\s]+))\s(("[^"]+")|[^\s]+)\s(?:-|"({user_agent}[^"]+)")\s(?:-|({action}[^-\s]+))""",
    ]
	ParserVersion = "v1.0.0"
  

}
```