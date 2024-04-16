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
Conditions = [ """ REJECT """ , """ vpc-""" ]
Fields = [
  """"eventTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
	"""({account_id}\d+)\s+REJECT"""
  """({action}REJECT)"""
  """REJECT(?:\s[^\s]+){1}\s({bytes}\d+)"""
  """REJECT(?:\s[^\s]+){2}\s(-|({dest_ip}(((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))))\s*({dest_port}\d+)?\s+({time}\d{10})"""
  """REJECT(?:\s[^\s]+){3}\s({dest_port}\d+)"""
  """REJECT(?:\s[^\s]+){4}\s({flow_end_time}\d+)"""
  """REJECT(?:\s[^\s]+){5}\s({direction}\S+)"""
  """REJECT(?:\s[^\s]+){6}\s({instance_id}[^\s]+)"""
  """REJECT(?:\s[^\s]+){7}\s({interface_id}[^\s]+)"""
  """REJECT(?:\s[^\s]+){8}\s({status_msg}[^\s]+)"""
  """REJECT(?:\s[^\s]+){9}\s({packets}\d+)"""
  """REJECT(?:\s[^\s]+){14}\s({protocol}[^\s]+)"""
  """REJECT(?:\s[^\s]+){15}\s({region}[^\s]+)"""
  """REJECT(?:\s[^\s]+){16}\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """REJECT(?:\s[^\s]+){17}\s({src_port}\d+)"""
  """REJECT(?:\s[^\s]+){18}\s({flow_start_time}\d+)"""
  """({tcp_flags}\S+)(?:\s[^\s]+){3}\svpc-"""
  """({vpc}vpc-[^\s]+)"""
]


}
```