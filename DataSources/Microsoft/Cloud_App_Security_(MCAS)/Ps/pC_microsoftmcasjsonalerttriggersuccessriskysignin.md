#### Parser Content
```Java
{
Name = microsoft-mcas-json-alert-trigger-success-riskysignin
Vendor = "Microsoft"
Product = "Cloud App Security (MCAS)"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """"src-event-id":""""
  """"entityType":"""
  """"title":""""
  """"app-username":""""
  """"context":"MCAS""""
]
Fields = [
  """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"src-ip":"({src_ip}[\da-fA-F:\.]+)""""
  """"title":"({alert_name}[^"]+)""""
  """"severity":({alert_severity}\d+),"""
  """"description":"({additional_info}.+?)"+,"+\w+"+:"""
  """"URL":"({malware_url}[^"]+)"+\}"""
  """app-username":"({user}[^"@]+)"""
  """"event-name":"({event_name}[^"]+)"""
  """user-email":"({email_address}[^\s@]+@({email_domain}[^"]+))"+\}"""
  """"app-user-displayname":"({full_name}[^"]+)"""
  """policyType":"({alert_type}[^"]+)""""
  """"raw-event":\{"_id":"({alert_id}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```