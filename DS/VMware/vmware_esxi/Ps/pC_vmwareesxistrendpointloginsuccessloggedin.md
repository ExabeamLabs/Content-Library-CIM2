#### Parser Content
```Java
{
Name = "vmware-esxi-str-endpoint-login-success-loggedin"
Vendor = "VMware"
Product = "VMware ESXi"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """ logged in """
  """ [User """
  """Event ["""
  """ vpxd """
]
Fields = [
  """({host}[^\s]+)\s+\d+\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """({host}[\w\-\.]+)\s*vpxd"""
  """User\s+((({domain}[^\\\s@]+)\\+)?({user}[^\s\\@]+)).+?\s*logged"""
  """\[({operation}User.+?logged (out|in))"""
  """user agent:\s+({user_agent}[^)]+)"""
  """\w+@(127.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  """Event \[([^\]]+\]\s+){3}\[([^\.]+\.){2}({event_name}[^\]]+)\]"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```