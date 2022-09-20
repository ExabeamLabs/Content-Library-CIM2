#### Parser Content
```Java
{
Name = cisco-securewebapp-str-http-session-squid
    Vendor = Cisco
    Product = Secure Web Appliance
    TimeFormat = "epoch_sec"
    Conditions = [ """cisco:wsa:squid"""]
    Fields = [
                """({time}\d{10})\.\d{3}""",
                """\s+({host}[^\s:]+):?\s+Info:""",
                """\d{10}\.\d{3}\s+[^\s]+\s(?:-|({src_ip}[^\s]+))""",
                """\d{10}\.\d{3}\s+([^\s]+\s){2}(?:-|({proxy_action}.+?)(\/(?:-|({http_response_code}\d+)))?)\s+""",
                """\d{10}\.\d{3}\s+([^\s]+\s){4}(?:-|({method}[^\s]+))""",
        """\d{10}\.\d{3}\s+([^\s]+\s){5}(?:-|({url}(({protocol}[^:]+):\/+)?[^\s:\/]+(:({dest_port}\d+))?\/(?:-|({uri_path}[^?\s]+))?({uri_query}\?[^\s]+)?))""",
                """\d{10}\.\d{3}\s+([^\s]+\s){6}"+(?:-|({domain}[^\\]+)\\+({user}[^@"]+))""",
                """\d{10}\.\d{3}\s+([^\s]+\s){5}(\w+:\/+)?({web_domain}(?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|[^\s\/:]+))""",
                """\d{10}\.\d{3}\s+([^\s]+\s){9}(?:-|({action}[^\s-]+))""",
                """\d{10}\.\d{3}\s+([^\s]+\s){8}(?:-|({mime}[^\s]+))""",
                """\d{10}\.\d{3}\s+([^\s]+\s){10}.*?"\s+({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+"""",
                """\s+<.+?>.+?\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\s+".+?"\s+"({category}[^"]+)""",
                """\d{10}\.\d{3}\s+([^\s]+\s){9}[^\s]+\s+<(?:-|nc|({category}[^,>]+))""",
                """\d{10}\.\d{3}\s+([^\s]+\s){9}[^\s]+\s+<[^>]+>\s+[^\s]+\s+"+(?:[\s-]|({user_agent}[^"]+))""",
    ]
	ParserVersion = "v1.0.0"
  

}
```