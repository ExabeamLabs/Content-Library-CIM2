#### Parser Content
```Java
{
Name = "forescout-counteract-kv-network-traffic-status"
  ParserVersion = "v1.0.0"
  Vendor = "Forescout"
  Product = "Forescout CounterACT"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""]: Log: Connection Status. Details: """
""" Connection Status: """
"""Vendor:"""
  ]
  Fields = [
"""(\w+\s+\d+ \d+:\d+:\d+)\s+({host}\S+)\s"""
"""Connection Status:\s+({action}({result}[^\s]+).+?)\.\s+Type"""
"""Source:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```