#### Parser Content
```Java
{
Name = "cisco-securewebapp-str-http-session-accesslog-1"
Vendor = "Cisco"
Product = "Cisco Secure Web Appliance"
TimeFormat = "epoch_sec"
Conditions = [
"""accesslog_ELK:"""
]
Fields = [
"""({time}\d{10})\.\d{3}"""
"""\d{10}\.\d{3}\s+\S+\s(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
"""\d{10}\.\d{3}\s+([^\s]+\s){2}(?:-|({proxy_action}.+?)(\/(?:-|({http_response_code}\d+)))?)\s"""
"""\d{10}\.\d{3}\s+([^\s]+\s){4}(?:-|({method}[^\s]+))"""
"""\d{10}\.\d{3}\s+([^\s]+\s){5}(?:-|({url}(({protocol}[^:]+):\/+)?[^\s:\/]+(:({dest_port}\d+))?\/(?:-|({uri_path}[^?\s]+))?({uri_query}\?[^\s]+)?))"""
"""\d{10}\.\d{3}\s+([^\s]+\s){6}"*(?:-|(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?))"""
"""\d{10}\.\d{3}\s+([^\s]+\s){5}(\w+:\/+)?({web_domain}(?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|[^\s\/:]+))"""
"""\d{10}\.\d{3}\s+([^\s]+\s){5}(?:-|({url}(({protocol}[^:]+):\/+)?[^\s:\/]+(:({dest_port}\d+))?\/(?:-|({uri_path}[^?\s]+))?({uri_query}\?[^\s]+)?))"""
"""\d{10}\.\d{3}\s+([^\s]+\s){9}(?:-|({action}[^\s-]+))"""
"""\d{10}\.\d{3}\s+([^\s]+\s){8}(?:["-]+|({mime}[^\s]+))"""
"""\Wdst\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\WdstPort\s*({dest_port}\d+)"""
"""\d{10}\.\d{3}\s+([^\s]+\s){9}[^\s]+\s+<(?:-|nc|({category}[^,>]+))"""
"""\Wuserag\s*"*(?:[\s-]|({user_agent}[^"]+))"""
]
ParserVersion = "v1.0.0"


}
```