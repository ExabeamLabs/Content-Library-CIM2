#### Parser Content
```Java
{
Name = cisco-iws-csv-http-session-tcpmissssl
  Vendor = Cisco
  Product = "Cisco Web Security"
  TimeFormat = "epoch_sec"
  ParserVersion = v1.0.0
  Conditions = ["""TCP_MISS_SSL""" ,"""AccessLogPush:""" ,""" 443 """]
  Fields = [
  """(\S{3}\s\d\d \d\d:\d\d:\d\d)\s+({host}\S+)\s+\S+\s+\S+\s+({time}\d{10})(.\d+)\s+(\d+)\s+(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+(?:-|({proxy_action}[^\s\/]+)\/({http_response_code}\d+))\s+(?:-|({bytes}\d+))\s+(?:-|unknown|({method}[^\s]+))\s"""
  ]
  

}
```