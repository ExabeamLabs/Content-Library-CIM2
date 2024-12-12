#### Parser Content
```Java
{
Name = "amazon-awsvpc-str-network-notification-success-nodata"
ParserVersion = v1.0.0
Vendor = "Amazon"
Product = "VPC Flow Logs"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
flow_start_timeFormat = ["epoch_sec"]
flow_end_timeFormat = ["epoch_sec"]
Conditions = [ """NODATA""" , """vpc-""" ]
Fields = [
  """cs6=\d+\s(-|({account_id}\d{12}))\s*(-|({vpc}vpc-[^\s]+))\s*\S+\s*(-|({interface_id}[^\s]+))\s*(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\s*(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\s*(-|({src_port}\d+))\s*(-|({dest_port}\d+))\s*(-|({protocol}[^\s]+))\s*(-|({packets}\d+))(\s*\S+\s*){2}(-|({tcp_flags}\S+))\s*\S+\s*(-|({bytes}\d+))\s*(-|({flow_start_time}\d+))\s*(-|({flow_end_time}\d+))\s*(-|({action}[^\s]+))\s*(-|({status_msg}[^\s]+))""",
	"""^(-|({account_id}\d{12}))\s*(-|({action}[^\s]+))\s*\S+\s*(-|({bytes}\d+))\s*(-|({dest_ip}(((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))))\s*(-|({dest_port}\d+))\s*(-|({flow_end_time}\d+))\s*(-|({direction}\S+))\s*(-|({instance_id}[^\s]+))\s*(-|({interface_id}[^\s]+))\s*(-|({status_msg}[^\s]+))\s*(-|({packets}\d+))\s*(\S+\s*){4}(-|({protocol}\d+))\s*(-|({region}[^\s]+))\s*(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\s*(-|({src_port}\d+))\s*(-|({flow_start_time}\d+))\s*(\S+\s*){3}(-|({tcp_flags}\S+))\s*(\S+\s*){3}(-|({vpc}[^\s]+))"""
]


}
```