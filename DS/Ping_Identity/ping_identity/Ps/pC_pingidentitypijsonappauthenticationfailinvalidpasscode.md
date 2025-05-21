#### Parser Content
```Java
{
Name = "pingidentity-pi-json-app-authentication-fail-invalidpasscode"
Vendor = "Ping Identity"
Product = "Ping Identity"
TimeFormat = "yyyy-dd-MM'T'HH:mm:ss.SSSZ"
Conditions = [ """"PINGID"""" , """Invalid One-Time Passcode""" , """"resources":""" , """"result":""" ]
Fields = [
  """"recorded":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
  """"actors":\s*\[[^\]]+?"type":\s*"user",[^\}]+"name":\s*"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
  """"ipaddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"source":\s*"({app}[^"]+)"""
  """"pingidmsg":\s*"({failure_reason}[^}\]]+?)\s*"[,\]}]"""
]
ParserVersion = "v1.0.0"


}
```