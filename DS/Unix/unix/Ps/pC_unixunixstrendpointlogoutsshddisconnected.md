#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-logout-sshddisconnected"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ 
    """ sshd["""
    """Disconnected from user"""
  ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
    """Disconnected from user (({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})) port ({src_port}\d+)""",
  ]
  ParserVersion = "v1.0.0"


}
```