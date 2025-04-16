#### Parser Content
```Java
{
Name = microsoft-mcas-json-alert-trigger-success-riskysignin
Vendor = "Microsoft"
Product = "Microsoft CAS"
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
  """"src-ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"title":"({alert_name}[^"]+?)(\\u200b)?"""""
  """"severity":({alert_severity}\d+),"""
  """"description":"({additional_info}.+?)"+,"+\w+"+:"""
  """"URL":"({malware_url}[^"]+)"+\}"""
  """app-username":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """"event-name":"({event_name}[^"]+)"""
  """user-email":"({email_address}[^\s@]+@({email_domain}[^"]+))"+\}"""
  """"app-user-displayname":"({full_name}[^"]+)"""
  """policyType":"({alert_type}[^"]+)""""
  """"raw-event":\{"_id":"({alert_id}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```