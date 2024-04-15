#### Parser Content
```Java
{
Name = "zscaler-ia-json-http-session-https"
Vendor = "Zscaler"
Product = "Zscaler Internet Access"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""","ologin":""""
""","cip":""""
""","url":""""
""","urlsupercat":""""
""","reqdatasize":"""
]
Fields = [
""""time":"({time}\d\d\d\d-\d\d-\d\d \d+:\d+:\d+)"""
""""ologin":"({email_address}({user}[^@\s"]+)@[^@\s"]+)""""
""""cip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""proto":"({protocol}[^"]+)"""
""""reqmethod":"({method}[^"]+)"""
""""url":"({url}[^"]+)"""
""""url":"(?:[^:]+:\/+)?({web_domain}[^\/:\s"]+)({uri_path}\/[^\?"]+)?({uri_query}\?[^"]+)?"""
""""respcode":"({http_response_code}\d+)"""
""""sip":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""action":"({action}[^"]+)"""
""""reason":"({proxy_action}[^"]+)"""
""""urlsupercat":"({category}[^"]+)"""
""""ua":"({user_agent}[^"]+)"""
""""referer":"({referrer}[^"]+)"""
""""fileclass":"({mime}[^"]+)"""
""""reqdatasize":({bytes_out}\d+)"""
""""respdatasize":({bytes_in}\d+)"""
]
ParserVersion = "v1.0.0"


}
```