#### Parser Content
```Java
{
Name = "vmware-vcenter-json-endpoint-login-success-userauthenticated"
Vendor = "VMware"
Product = "vCenter"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """ VIEWCENTER """
  """Authenticated user"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """host":"({host}[^"]+)"""
  """vim.event.({operation}[^\s\]]+)"""
  """Authenticated user ({user}[\w\.\-]{1,40}\$?)"""
  """({app}VM_VCenter)"""
]
ParserVersion = "v1.0.0"


}
```