#### Parser Content
```Java
{
Name = "vmware-esxi-str-endpoint-login-success-loggedin-1"
Vendor = "VMware"
Product = "VMware ESXi"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """]["""
  """ User """
  """ logged in """
  """ESX"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d).+?\s+({dest_host}({host}[\w\-\.]+))\s""",
  """User\s+((({domain}[^\\\s@]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)).+?\s*logged""",
  """({operation}({event_name}logged in))""",
  """:\s+({additional_info}User.+?)\s*$"""
  """logged in\s*as\s*({user_agent}.+?)\s*$""",
  """({app}ESX)"""
]
ParserVersion = "v1.0.0"


}
```