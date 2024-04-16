#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-notification-success-systemerror"
  Vendor = "Unix"
  Product = "Unix"
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
  """System error"""
  """pam_sss(sudo:auth)"""
  """received for user"""
  ]
  Fields = [
  """({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """({host}[\w\.\-]+)?:?\s*sudo"""
  """\suser\s*((NT AUTHORITY|({domain}[^\\"]+))[\\\/]+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""
  """received for user ({account}[\w\.\-]{1,40}).+?\(({additional_info}[^\)]+?)\)"""
  ]


}
```