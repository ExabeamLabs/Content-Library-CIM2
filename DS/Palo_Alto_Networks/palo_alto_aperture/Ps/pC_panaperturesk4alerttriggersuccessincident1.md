#### Parser Content
```Java
{
Name = pan-aperture-sk4-alert-trigger-success-incident-1
Vendor = Palo Alto Networks
Product = Palo Alto Aperture
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """"incident""""
  """"cloud_app_instance""""
  """"item_owner":""""
  """"item_creator_email":"""
  """"item_verdict":"malware""""
]
Fields = [
  """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""""
  """"policy_rule_name":"({alert_name}[^"]+)""""
  """"item_verdict":"({alert_type}[^"]+)""""
  """"severity":({alert_severity}[\d\.]+)"""
  """"item_creator":"(Possible External Application Or Not Logged In User|({full_name}[^"]+))""""
  """"item_creator_email":"(Unknown|({email_address}[^\s",@]+\@[\w\.\-]+))""""
  """"item_name":"({file_name}[^"]+)""""
  """"item_cloud_url":"({malware_url}[^"]+)""""
  """"incident_id":"({alert_id}[^"]+)""""
  """"item_sha256":"({file_hash}[^"]+)""""
  """msg=({additional_info}[^=]+)\s\w+="""
]
ParserVersion = "v1.0.0"


}
```