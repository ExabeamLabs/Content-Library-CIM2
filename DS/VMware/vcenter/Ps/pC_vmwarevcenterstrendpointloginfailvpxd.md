#### Parser Content
```Java
{
Name = "vmware-vcenter-str-endpoint-login-fail-vpxd"
Vendor = "VMware"
Product = "vCenter"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
  """vpxd["""
  """] Event ["""
  """[error]"""
  """[Cannot login"""
  """[vim.event"""
]
Fields = [
  """\[({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\]"""
  """\d\d:\d\d:\d\d\s({src_host}[^\s]+) vpxd\["""
  """\[vim.event.({failure_reason}[^\]]+)\]"""
  """\[Cannot login (user )?(({domain}[^\\]+)\\({user}[^@]+)|({=user}[^@]+)@({=domain}[^@]+))@({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?(:\s({failure_reason}[^\]]+))?\]"""
]
ParserVersion = "v1.0.0"


}
```