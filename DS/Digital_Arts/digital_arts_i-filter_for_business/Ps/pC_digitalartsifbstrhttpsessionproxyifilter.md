#### Parser Content
```Java
{
Name = "digitalarts-ifb-str-http-session-proxyifilter"
Vendor = "Digital Arts"
Product = "Digital Arts i-FILTER for Business"
TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
Conditions = [
  """[proxyIfilter:"""
]
Fields = [
  """\w+ \d+ \d\d:\d\d:\d\d \d+ \S+ (-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?) (-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?) (-|({src_host}\S+)) (-|({user}[\w\.\-]{1,40}\$?)) \[({time}\d+\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d [+-]\d+)\] ({http_response_code}\d+) ({bytes_out}\d+) ({bytes_in}\d+) ({action}\S+) \S+ ({result_reason}\S+) ({category}\S+)[^\"]+?\"+({method}\S+) ({url}(({protocol}\w+):[\\\/]+)?({web_domain}[^\\\/\s:]+)({uri_path}\/[^\s\?]+)?({uri_query}\?[^\s\"]+)?)[^\"]*\"+ (-|({referrer}\S+)) (-|({user_agent}[^\"]+?)) \S+ \S+\s*$"""
]
ParserVersion = "v1.0.0"


}
```