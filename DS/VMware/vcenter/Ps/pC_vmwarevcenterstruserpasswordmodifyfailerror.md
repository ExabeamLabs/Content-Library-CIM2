#### Parser Content
```Java
{
Name = vmware-vcenter-str-user-password-modify-fail-error
  Vendor = VMware
  Product = vCenter
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
  Conditions = [ """:Error:""", """Failed to change """, """error =""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,6})[^\s]+\s+({host}[\w\-.]+)\s+({process_name}\S+)\s({process_id}\d+)"""
    """Error:\s*({failure_reason}[^"\)]+\)*)$"""
    """machine password for\s*({domain}[^"\s]+)"""
    """error\s+=\s+({error_code}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```