#### Parser Content
```Java
{
Name = "squid-s-str-http-session-squid"
Vendor = "Squid"
Product = "Squid"
TimeFormat = "epoch_sec"
Conditions = [
""" (squid): """
]
Fields = [
"""({host}\S+)\s\(squid\):\s+({time}\d{10})[\.\d]+\s+\d+\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s(\w+\/)?({http_response_code}\d+)\s({bytes_out}\d+)\s(({method}GET|CONNECT|HEAD|POST|PUT|DELETE|OPTIONS|TRACE)|\S+)\s(error:invalid-request|((({url}[^:]+:\/\/(({web_domain}[^:\s]+)?(:({dest_port}\d+))|[^\s]+))?))|(({=web_domain}[^:\s])+?(:({=dest_port}\d)+))|({uri_path}[^\s]+?)({uri_query}\?[^\s]+)?)\s(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s(\S+\/)?(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({=dest_port}\d)+)?)\s(-|({mime}[^\s$]+))\s*$"""
]
ParserVersion = "v1.0.0"


}
```