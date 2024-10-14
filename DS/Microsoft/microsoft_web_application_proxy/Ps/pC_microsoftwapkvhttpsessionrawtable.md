#### Parser Content
```Java
{
Name = "microsoft-wap-kv-http-session-rawtable"
Vendor = "Microsoft"
Product = "Microsoft Web Application Proxy"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" UrlDestHost:"""
"""RawTable:"""
""" uri:"""
]
Fields = [
"""ClientUserName:\s*"(?:anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
"""ClientAgent:\s*"({user_agent}[^"]+)""""
"""logTime:\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""servername:\s*"({host}[^"]+)""""
"""bytesrecvd:\s*"({bytes_in}\d+)"""
"""bytessent:\s*"({bytes_out}\d+)"""
"""transport:\s*"({protocol}[^"]+)""""
"""Action:\s*"({action}[^"]+)""""
"""DecryptedIP:\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""UrlDestHost:\s*"({web_domain}[^"]+)""""
"""DestHostPort:\s*"({dest_port}\d+)""""
"""mimetype:\s*"(?:-|({mime}[^"]+))""""
"""operation:\s*"(?:-|({method}[^"]+))""""
"""uri:\s*"(?:-|((\w+:\/+)?[^\/]+\/({uri_path}.+?)))(\?|")"""
"""uri:\s*"(?:-|((\w+:\/+)?[^?]+({uri_query}\?.+?)))""""
]
ParserVersion = "v1.0.0"


}
```