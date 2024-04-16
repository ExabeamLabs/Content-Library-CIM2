#### Parser Content
```Java
{
Name = "squid-s-str-http-session-squidaccess"
Vendor = "Squid"
Product = "Squid"
TimeFormat = "epoch_sec"
Conditions = [
"""squid-access-default:"""
]
Fields = [
"""({host}\S+)\s+squid-access-default:\s+({time}\d{10})\.\d{3}\s+({duration}\d+)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+(?:\w+\/)({http_response_code}\d+)\s+({bytes_out}\d+)\s+({method}\S+)\s+(?:\w+\:\/+)?(?:({dest_host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({web_domain}[^\s:\/]+))(?:\:({dest_port}\d+))?\S*?\s+({user}[\w\.\-]{1,40}\$?)\s+({hierarchy_code}[^\/]+)\/({forwarded_host}[^\/\s]+)\s"""
]
ParserVersion = "v1.0.0"


}
```