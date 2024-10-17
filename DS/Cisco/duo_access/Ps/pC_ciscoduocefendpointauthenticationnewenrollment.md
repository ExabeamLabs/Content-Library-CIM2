#### Parser Content
```Java
{
Name = "cisco-duo-cef-endpoint-authentication-newenrollment"
  Vendor = "Cisco"
  Product = "Duo Access"
  TimeFormat = "epoch_sec"
  Conditions = [ """"username":""", """"device":""", """"factor":""", """"integration":""", """"new_enrollment":""" ]
  Fields = [
"""\"isotimestamp\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}([+-]\d\d:\d\d)?)\""""
"""\"timestamp\":\s*({time}\d{10})"""
"""\"integration\":\s*\"({app}[^\"]+)"""
"""\"factor\":\s*\"(?:(n\/a)|({operation}[^\"]+))\"""",
"""\"username\"\s*:\s*\"(?!AD Sync:)(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({full_name}[^\s\"]+\s[^\"]+)|((?:({domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
"""\"device\":\s*\"({object}[^\"]+)"""
"""\"email\":\s*\"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""
"""\"ip(_address)?\":\s*\"(0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\""""
"""\"result\":\s*\"({result}[^\"]+)"""
"""\"browser\":\s*\"((?i)unknown|({browser}[^\"]+))"""
"""\"os\":\s*\"({os}[^\"]+)"""
"""\"city\":\s*\"({city}[^\"]+)"""
"""\"state\":\s*\"({state}[^\"]+)"""
"""\"country\":\s*\"({country}[^\"]+)"""
"""\"reason\":\s*\"(({event_name}(?i)User approved|Valid passcode|Remembered device|Trusted network)|({failure_reason}[^\"]+))"""
"""User email:\s*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
""""new_enrollment"\s*:\s*({new_enrollment}[^,]+?),[\s"\w]+?:""",
""""host"\s*:\s*"({host}[^,"]+?)"""",
""""reason"\s*:\s*"({failure_reason}[^"]+)"[^=]+?"result":"(denied|fraud|failure|error)"""",
""""result"\s*:\s*"(denied|fraud|failure|error)"[^=]+?"reason":"({failure_reason}[^"]+)"""",
  ]
  DupFields = [ "object->device_name", "app->service_name", "operation->auth_method", "operation->factor","country->mfa_country", "object->mfa_device", "result->action" ]
  ParserVersion = "v1.0.0"


}
```