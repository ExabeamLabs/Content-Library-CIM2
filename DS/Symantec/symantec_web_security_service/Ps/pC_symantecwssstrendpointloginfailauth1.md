#### Parser Content
```Java
{
Name = "symantec-wss-str-endpoint-login-fail-auth-1"
  Vendor = "Symantec"
  Product = "Symantec Web Security Service"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ProxySG:""", """ Authentication failed with""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """:\d\d:\d\d ({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))? """
    """({host}[\w.-]+) ProxySG:"""
    """({event_name}Authentication failed)"""
    """ user '(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))' \(domain (\(null\)|({domain}[^\)]+))\)"""
    """symbol: '({failure_reason}[^']+)"""
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```