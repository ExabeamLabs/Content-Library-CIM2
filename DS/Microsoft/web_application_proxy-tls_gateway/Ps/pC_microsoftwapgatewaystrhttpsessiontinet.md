#### Parser Content
```Java
{
Name = "microsoft-wapgateway-str-http-session-tinet"
Vendor = "Microsoft"
Product = "Web Application Proxy-TLS Gateway"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """\tInet\t"""
  """\tReq ID:"""
]
Fields = [
  """(?:-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)[\s\,]+[\w\s]+[\t\,]+(?:None|Web Proxy)[\t\,]+({web_domain}[^\t\,]+)"""

]
ParserVersion = "v1.0.0"


}
```