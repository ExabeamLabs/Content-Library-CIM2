#### Parser Content
```Java
{
Name = zimperium-mtd-json-alert-trigger-success-threatuuid
  Vendor = Zimperium
  Product = Zimperium MTD
  ParserVersion = "v1.0.0"
  TimeFormat = "dd MM yyyy HH:mm:ss z"
  Conditions = [ """"zapp_instance_id":""",""""threat_type":""",""""threat_uuid":""",""""device_info":""" ]
  Fields = [
  """eventtimestamp":\s"({time}\d\d\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d\s\w{1,3})"""
	"""user_email":\s"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
	"""employee_name":\s"({full_name}[^"\}]+)"""
	"""device_ip":\s"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
	"""severity":\s({alert_severity}\d{1,5})"""
	"""event_id":\s"({alert_id}[^"]+)"""
	"""story":\s"({additional_info}[^",]+)"""
	"""threat_type":\s"({alert_type}[^",]+)"""
	"""Threat.+?"name":\s"({alert_name}[^"]+)"""
  ]


}
```