#### Parser Content
```Java
{
Name = f5-bigip-str-http-traffic-success-httpproxy
  Vendor = F5
  Product = F5 BIG-IP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ParserVersion = v1.0.0
  Conditions = [ """info tmm""", """/Common/http_proxy_vs""", """/Common/proxy_class""" ]
  Fields = [
  """\d\d:\d\d:\d\d ({host}[^\s]+)""",
  """info tmm[^:]+:([^,]+.){1}"({src_host}[^"]+)","({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","({src_port}\d+)","({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))","({dest_port}\d+)","({protocol}[^"]+)",("[^,]+,){4}"({action}[^"]+)","[^"]+","({method}[^"]+)"""
  ]


}
```