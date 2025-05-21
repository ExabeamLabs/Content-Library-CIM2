#### Parser Content
```Java
{
Name = "digitalarts-ifb-csv-http-session-proxy"
Vendor = "Digital Arts"
Product = "Digital Arts i-FILTER for Business"
TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
Conditions = [
"""Digital Arts"""
"""i-FILTER Proxy Server"""
]
Fields = [
  """\[({time}\d+\/\w+\/\d+:\d\d:\d\d:\d\d[^\]]+)\]"""
  """\d+\]\s+({http_response_code}\d+?)\s"""
  """\d+\]\s+([^\s+]+\s){1}({bytes_out}\d+?)\s"""
  """\d+\]\s+([^\s+]+\s){2}({bytes_in}\d+?)\s"""
  """\d+\]\s+([^\s+]+\s){3}({action}[^\s]+?)\s"""
  """\d+\]\s+([^\s+]+\s){4}({result_reason}[^\s]+?)\s"""
  """\d+\]\s+([^\s+]+\s){5}({category}[^\s]+?)\s"""
  """({method}GET|POST|PUT|TUNNEL|OPTIONS|CONNECT|HEAD|DELETE)\s*({url}(({protocol}\w+):[\\\/]+)?({web_domain}[^\\\/\s:]+)({uri_path}\/[^\s\?]+)?({uri_query}\?[^\s"]+)?)[^"]*"+\s*(-|({referrer}\S+))\s*(-|({user_agent}[^"]+))\s(-|({mime}\S+))(\s\S+){2}(\w+=|$)"""
  """:\d\d:\d\d\s*\d+\s*\S+\s*([^\s+]+\s){1}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s"""
]
ParserVersion = "v1.0.0"


}
```