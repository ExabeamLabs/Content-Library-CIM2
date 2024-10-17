#### Parser Content
```Java
{
Name = "vmware-vcenter-json-endpoint-login-success-userauthenticated"
Vendor = "VMware"
Product = "vCenter"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
ExtractionType = json
Conditions = [
  """ VIEWCENTER """
  """Authenticated user"""
]
Fields = [
  """exa_regex=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """exa_json_path=$.host,exa_field_name=host"""
  """exa_json_path=$.message,exa_regex=Authenticated user ({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """exa_regex=({app}VM_VCenter)"""
]
ParserVersion = "v1.0.0"


}
```