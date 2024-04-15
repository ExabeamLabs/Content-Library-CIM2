#### Parser Content
```Java
{
Name = "cisco-securewebapp-str-http-session-accesslog"
Vendor = "Cisco"
Product = "Cisco Secure Web Appliance"
TimeFormat = "epoch_sec"
Conditions = [
"""accesslog_syslog:"""
]
Fields = [
"""accesslog_syslog:\s\S+\s({time}\d{10})\.\d{3}\s\S+\s({src_ip}[\d.:a-fA-F]+)\s((-|(?i)NONE|({proxy_action}[^\s\/]+?))(\/(-|({http_response_code}\d+)))?)\s\d+\s(-|({method}[^\s]+))"""
"""accesslog_syslog:(\s\S+){7}\s(-|({url}(({protocol}[^:]+):\/+)?[^\s:\/]+(:({dest_port}\d+))?\/(?:-|({uri_path}[^?\s]+))?({uri_query}\?[^\s]+)?))"""
"""accesslog_syslog:(\s\S+){8}\s"*(-|(({domain}[^\\]+)[\\\/]+)?({user}[^@"\s]+))"""
"""accesslog_syslog:(\s\S+){7}\s(\w+:\/+)?({web_domain}(?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|[^\s\/:]+))"""
"""accesslog_syslog:(\s\S+){11}\s(-|({action}[^\s-]+))"""
"""accesslog_syslog:(\s\S+){10}\s(["-]+|({mime}[^\s]+))"""
"""\Wdst\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\WdstPort\s*({dest_port}\d+)"""
"""accesslog_syslog:(\s\S+){12}\s<(["-]+|nc|({category}[^,>]+?))\s*[,>]"""
"""\Wuserag\s*"*(?:[\s-]|({user_agent}[^"]+))"""
]
ParserVersion = "v1.0.0"


}
```