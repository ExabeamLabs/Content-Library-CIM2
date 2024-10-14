#### Parser Content
```Java
{
Name = "microsoft-wapgateway-json-http-session-reqid"
Vendor = "Microsoft"
Product = "Web Application Proxy-TLS Gateway"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """Web Proxy"""
  """Req ID:"""
]
Fields = [
  """({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})[\t\,]+(?:anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))[\t\,]+(?:-|({user_agent}.+?))[\t\,]+({time}\d{4}-\d{2}-\d{2}[\s]+\d{2}:\d{2}:\d{2})(?:[\t\,]+(?:Y|N))?[\t\,]+({host}[\w\-_]+)[\t\,]+[^\t\,]+[\s\,]+(?:-|({dest_host}[\w\-_.]+))[\t\,]+(?:-|({dest_ip}[^\t\,]+))[\t\,]+({dest_port}\d+)[\t\,]+\d+[\t\,]+(?:-|({bytes_out}\d+))[\t\,]+(?:-|({bytes_in}\d+))[\t\,]+({protocol}[\w-]+)[\t\,]+(?:-|({method}\w+))[\t\,]+(?:({url}(\w+:\/{2})?(({=dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({web_domain}[^\t\/]*?))(:({=dest_port}\d+))?({uri_path}\/[^?\s]*)?({uri_query}\?[^\t\s\,]*)?))[\t\,]+(?:(?:-|({mime}[^\t\,]+))[\t\,]+(?:-|Inet|VFInet|0)[\t\,]+(?:-|({http_response_code}\d+)).+[\t\,]+Req ID.+\s({error_code}0x\d+)[\t\,]+({action}\w+))?"""
]
ParserVersion = "v1.0.0"


}
```