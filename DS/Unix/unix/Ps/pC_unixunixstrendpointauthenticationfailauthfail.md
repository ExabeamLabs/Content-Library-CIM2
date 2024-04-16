#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-authentication-fail-authfail"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
  """Authentication failure"""
  """pam_sss(sudo:auth)"""
  ]
  Fields = [
  """({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """({host}[\w\.\-]+)?:?\s*sudo"""
  """\suser\s*((NT AUTHORITY|({domain}[^\\"]+))[\\\/]+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""
  """({result}failure)"""
  ]
  ParserVersion = "v1.0.0"


}
```