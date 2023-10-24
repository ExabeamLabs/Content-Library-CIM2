#### Parser Content
```Java
{
Name = "amazon-awsvpc-str-network-traffic-fail-reject"
ParserVersion = v1.0.0
Vendor = "Amazon"
Product = "VPC Flow Logs"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
flow_start_timeFormat = ["epoch_sec"]
flow_end_timeFormat = ["epoch_sec"]
Conditions = [ """REJECT""" , """vpc-""" ]
Fields = [
  """"eventTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
	"""({account_id}\d+)\s+REJECT"""
  """({action}REJECT)"""
  """REJECT(?:\s[^\s]+){1}\s({bytes}\d+)"""
  """REJECT(?:\s[^\s]+){2}\s(-|({dest_ip}(((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))))\s*({dest_port}\d+)?"""
  """REJECT(?:\s[^\s]+){3}\s({dest_port}\d+)"""
  """REJECT(?:\s[^\s]+){4}\s({flow_end_time}\d+)"""
  """REJECT(?:\s[^\s]+){5}\s({direction}\S+)"""
  """REJECT(?:\s[^\s]+){6}\s({instance_id}[^\s]+)"""
  """REJECT(?:\s[^\s]+){7}\s({interface_id}[^\s]+)"""
  """REJECT(?:\s[^\s]+){8}\s({status_msg}[^\s]+)"""
  """REJECT(?:\s[^\s]+){9}\s({packets}\d+)"""
  """({protocol}\d+)(?:\s[^\s]+){11}\svpc-"""
  """({region}[^\s]+)(?:\s[^\s]+){10}\svpc-"""
  """({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(?:\s[^\s]+){9}\svpc-"""
  """({src_port}\d+)(?:\s[^\s]+){8}\svpc-"""
  """({flow_start_time}\d+)(?:\s[^\s]+){7}\svpc-"""
  """({tcp_flags}\S+)(?:\s[^\s]+){3}\svpc-"""
  """({vpc}vpc-[^\s]+)"""
]


}
```