#### Parser Content
```Java
{
Name = "pingidentity-pi-json-endpoint-app-activity-success"
  ParserVersion = "v1.0.0"
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [""""app":"ping-cloud"""", """"kubernetes":""", """"container_name"""", """"log_group":"application"""", """"stream":"stdout"""" ]
  Fields  = [
	""""@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\dZ)"""
  """"log":.+?"host":"({host}[^"]+)"""
	""""container_image":"({image_name}[^"]+)"""",
	""""role":"({service_name}[^"]+)""",
	""""app":"({app}[^"]+)"""
	""""pod_id":"({instance_id}[^"]+)"""
	"""requesterIP=\\*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
	"""resultCodeName =\\*"({result}[^"\\]+)\\*""""
  ]


}
```