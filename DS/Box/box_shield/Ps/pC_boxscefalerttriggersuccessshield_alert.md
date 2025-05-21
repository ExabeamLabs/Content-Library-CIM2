#### Parser Content
```Java
{
Name = box-s-cef-alert-trigger-success-shield_alert
  Vendor = "Box"
  Product = "Box Shield"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """destinationServiceName =Box""", """"item_type":"""", """"item_name":""", """"event_type":""", """"SHIELD_ALERT",""", """"rule_category":""" ]
  Fields = [
	""""created_at":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d([\+\-]\d\d:\d\d)?)""",
	""""event_type":"({event_subtype}[^"]+)"""",
	""""user":\{[^\}]*?"id":({user_id}[^"]+),""",
	""""user":\{[^\}]*?"name":"({full_name}[^"]+)"""",
	""""user":\{[^\}]*?"email":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
	""""additional_details":\{.*?"shield_alert":\{[^\}]*?"rule_category":"({alert_type}[^"]+)"""",
	""""additional_details":\{.*?"shield_alert":\{[^\}]*?"rule_id":"({alert_id}[^"]+)"""",
	""""additional_details":\{.*?"shield_alert":\{[^\}]*?"rule_name":"({alert_name}[^"]+)"""",
	""""priority":"({alert_severity}[^"]+)"""",
	""""alert_summary":\{[^\}]*?"event_type":"({operation}[^"]+)"""",
	""""item_name":"({malware_file_name}[^"]+)""""
	""""item_type":"({malware_file_type}[^"]+)"""
	""""item_path":"({file_dir}[^"]+)""""
	"""additional_details":\{[^\}]*?"size":({bytes}\d+)"""
	""""service_name":"({service_name}[^"]+)"""
	""""hash":"({hash_sha1}^"]+)","hash_type":"({hash_type}sha1)"""",
	""""hash":"({hash_sha256}^"]+)","hash_type":"({hash_type}sha256)"""",
	""""ip_info":\{([^\}]*?)"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
]
ParserVersion = "v1.0.0"


}
```