#### Parser Content
```Java
{
Name = "sigsci-sigsci-json-http-session-servername"
Vendor = "SIGSCI"
Product = "SIGSCI"
TimeFormat = "yyyy-MM-dd'T'HH:ss:SSZ"
Conditions = [
""""serverHostName"=""""
""""remoteHostname"=""""
""""serverName"=""""
""""uri"=""""
]
Fields = [
""""+serverName"+="+({host}[\w\.-]+)"""
""""+serverHostName"+="+({dest_host}[^"]+)"""
""""+remoteIP"+="+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""+remoteHostname"+="+(,|({src_host}[^"]+))"""
""""+userAgent"+="+(,|({user_agent}[^"]+))"""
""""+timestamp"+="+({time}[^"]+)"""
""""+method"+="+(,|({method}[^"]+))"""
""""+path"+="+({uri_path}[^"]+)"""
""""+responseCode"+="+({http_response_code}\d+)"""
""""+protocol"+="+(,|({protocol}[^"]+))"""
""""+responseSize"+="+({bytes_out}\d+)"""
]
ParserVersion = "v1.0.0"


}
```