#### Parser Content
```Java
{
Name = "cisco-duo-cef-endpoint-authentication-newenrollment"
  Vendor = "Cisco"
  Product = "Duo Access"
  TimeFormat = "epoch_sec"
  Conditions = [
""" destinationServiceName =DUO """
"""dproc=authentication-logs"""
""""new_enrollment""""
]
  Fields = [
"""\"isotimestamp\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}([+-]\d\d:\d\d)?)\""""
"""\"timestamp\":\s*({time}\d{10})"""
"""\"integration\":\s*\"({app}[^\"]+)"""
"""\"factor\":\s*\"(?:(n\/a)|({operation}[^\"]+))\""""
"""\"username\":\"(?!AD Sync:)(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}[^\s\"]+\s[^\"]+)|({user}[^\"]+))"""
"""\"device\":\s*\"({object}[^\"]+)"""
"""\"email\":\s*\"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""
"""\"ip(_address)?\":\s*\"(0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\""""
"""\"result\":\s*\"({result}[^\"]+)"""
"""\"browser\":\s*\"((?i)unknown|({browser}[^\"]+))"""
"""\"os\":\s*\"({os}[^\"]+)"""
"""\"city\":\s*\"({city}[^\"]+)"""
"""\"state\":\s*\"({state}[^\"]+)"""
"""\"country\":\s*\"({country}[^\"]+)"""
"""\"reason\":\s*\"(({event_name}(?i)User approved|Valid passcode|Remembered device|Trusted network)|({failure_reason}[^\"]+))"""
  ]
  DupFields = [ "object->device_name", "app->service_name", "operation->auth_method", "operation->factor" ]
  ParserVersion = "v1.0.0"


}
```