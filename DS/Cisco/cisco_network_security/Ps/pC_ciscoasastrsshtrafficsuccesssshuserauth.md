#### Parser Content
```Java
{
Name = "cisco-asa-str-ssh-traffic-success-sshuserauth"
Vendor = "Cisco"
Product = "Cisco Network Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","MMM dd HH:mm:ss.SSS", "MMM  d HH:mm:ss.SSS"]
Conditions = [
  """%SSH-"""
  """SSH2_USERAUTH:"""
]
Fields = [
  """({event_code}%SSH-[^:]+)"""
  """({host}[\w\.\-]+): ({time}\w\w\w\s*\d+\s*\d\d:\d\d:\d\d\.\d\d\d): %SSH-5-SSH2_USERAUTH"""
  """SSH2_USERAUTH:\s*User '(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))' authentication for SSH2 Session from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """({result}Succeeded|Failed)"""
]
ParserVersion = "v1.0.0"


}
```