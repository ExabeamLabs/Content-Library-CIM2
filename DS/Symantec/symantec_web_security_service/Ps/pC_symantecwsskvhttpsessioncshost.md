#### Parser Content
```Java
{
Name = "symantec-wss-kv-http-session-cshost"
Vendor = "Symantec"
Product = "Symantec Web Security Service"
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = [
"""action="""
"""TCP"""
"""cs_host"""
"""cs_method="""
"""src_ip"""
]
Fields = [
"""Time="({time}\d+/\d+/\d+\s\d+:\d+:\d+)"""
"""user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""action="?({action}[^"\s,]+)"""
"""src_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""Browser="({browser}[^"]+)"""
"""cs_host="({web_domain}([^\s]+\.)?([^"]+))""""
"""cs_method="({method}[^"]+)"""
"""bytes_out=({bytes_out}\d+)"""
"""bytes_in=({bytes_in}\d+)"""
"""category="({category}[^"]+)"""
"""OS="({os}[^"]+)"""
"""cs_uri_query="*(|({uri_query}[^"]+))""""
"""http_referrer="*(|({referrer}[^"]+))""""
"""latest\(url\)="*(|({url}[^"]+))""""
]
ParserVersion = "v1.0.0"


}
```