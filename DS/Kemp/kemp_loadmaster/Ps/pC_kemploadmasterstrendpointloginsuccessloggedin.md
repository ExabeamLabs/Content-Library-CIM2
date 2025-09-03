#### Parser Content
```Java
{
Name = "kemp-loadmaster-str-endpoint-login-success-loggedin"
Vendor = "Kemp"
Product = "Kemp LoadMaster"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """logger: User"""
  """ Logged in """
  """(Session: """
]
Fields = [
  """User\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\)"""
  """({event_name}Logged in)"""
  """({event_category}logger)"""
]
ParserVersion = "v1.0.0"


}
```