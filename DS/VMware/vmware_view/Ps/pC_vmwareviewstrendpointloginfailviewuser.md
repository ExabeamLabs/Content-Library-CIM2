#### Parser Content
```Java
{
Name = "vmware-view-str-endpoint-login-fail-viewuser"
Vendor = "VMware"
Product = "VMware View"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """View User"""
  """has logged in to a new session on machine"""
]
Fields = [
  """\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+View User"""
  """View User\s+(({domain}[^\\\s]+)\\+)?({user}[\w\.\-]{1,40}\$?)"""
  """({app}View)"""
  """new session on machine\s+({dest_host}[\w.-]+)"""
]
ParserVersion = "v1.0.0"


}
```