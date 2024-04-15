#### Parser Content
```Java
{
Name = "edgewave-iprism-str-http-session-web"
Vendor = "EdgeWave"
Product = "EdgeWave iPrism"
TimeFormat = "epoch_sec"
Conditions = [
""" iPrism["""
"""]: WEB"""
]
Fields = [
"""Original Address=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\]: WEB\s+({protocol}\S+)\s+({time}\d{10})\s+({result}\S+)\s+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({proxy_action}\S+)\s+(\[[^\]]*\]|((({domain}[^\\\s\[\]]+)\\+)?({user}[^\\\s\[\]]+)))\s+\S+\s+({categories}({category}[^;,]+)[^\s]+)\s+\d+\s+({method}\S+)\s+({http_response_code}\d+)\s+\S+\s+(-|({url}(({=protocol}[^:\\\/\s,"]+):[\\\/]+)?({web_domain}[^\\\/\s:,"]+)?(:({dest_port}\d+))?({uri_path}\/[^\s\?",]*)?({uri_query}\?[^"\s,]*)?))\s+$"""
]
ParserVersion = "v1.0.0"


}
```