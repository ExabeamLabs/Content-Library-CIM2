#### Parser Content
```Java
{
Name = sailpoint-identitynow-json-app-authentication-login
  Vendor = Sailpoint
  Product = IdentityNow
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """"type":"AUTH"""", """"stack":""", """"attributes":""", """"info":"LOGIN_""" ]
  Fields = [
     """"created":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3})"""
     """"hostName":"(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[\w\-\.]+))""""
     """"actor":[^\}]+?"name":\s*"((?i)Not Available|unknown|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|(({full_name}[^\s"]+\s[^"]+)|({user}[\w\.\-]{1,40}\$?)))""""
     """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
     """"info":"(NONE|({additional_info}[^",]+))""""
     """"operation":"({operation}[^"]+)""""
     """"status":"({result}[^"]+)"""",
     """"sourceName":"({app}[^"]+)""""
     """"name":"({event_name}[^"]+?)\s*",""""
  ]
  ParserVersion = "v1.0.0"


}
```