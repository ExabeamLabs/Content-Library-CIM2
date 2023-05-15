#### Parser Content
```Java
{
Name = f5-waf-str-network-traffic-fail-warningtmm
  Vendor = F5
  Product = F5 Advanced Web Application Firewall
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
	"""F5-DMZ""" 
	"""warning tmm["""
]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[^\s]+)""",
	  """warning tmm\[({process_id}\d+)\]"""
	  """warning tmm\[\d+\]:\s+[\d:]+\s+({failure_reason}[^;(]+)"""
    """({failure_reason}Connection error:[^:\d]+)"""
    """({failure_reason}Per IP in-progress sessions limit \(128\) exceeded)"""
    """originating from IP\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """warning[^->]+\s+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))[^:]*(:({src_port}\d+))? -> ({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))[^:]*(:({dest_port}\d+))?"""
	  """exceeded for\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```