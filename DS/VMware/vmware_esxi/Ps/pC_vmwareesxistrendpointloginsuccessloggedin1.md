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
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d).+?\s+({host}[^\s]+)\s""",
  """User\s+((({domain}[^\\\s@]+)\\+)?({user}[^\s\\@]+)).+?\s*logged""",
  """({event_name}logged in)""",
  """:\s+({additional_info}User.+?)\s*$"""
  """logged in\s*as\s*({user_agent}.+?)\s*$""",
  """({app}ESX)"""
]
DupFields = [
  "event_name->operation"
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```