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
	"""(-|({account_id}\d{12}))\s*(-|({action}[^\s]{2,}))\s*\S+\s*(-|({bytes}\d+))\s*(-|({dest_ip}(((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))))\s*(-|({dest_port}\d+))\s*(-|({flow_end_time}\d+))\s*(-|({direction}\S+))\s*(-|({instance_id}[^\s]+))\s*(-|({interface_id}[^\s]+))\s*(-|({status_msg}[^\s]+))\s*(-|({packets}\d+))\s*\S+\s*\S+\s*\S+\s*\S+\s*(-|({protocol}\d+))\s*(-|({region}[^\s]+))\s*(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\s*(-|({src_port}\d+))\s*(-|({flow_start_time}\d+))\s*(\S+\s*){3}(-|({tcp_flags}\S+))\s*(\S+\s*){3}(-|({vpc}[^\s]+))"""
]


}
```