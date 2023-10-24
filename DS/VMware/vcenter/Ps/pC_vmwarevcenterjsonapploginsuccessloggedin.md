#### Parser Content
```Java
{
Name = vmware-vcenter-json-app-login-success-loggedin
  Vendor = VMware
  Product = vCenter
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"Message":""" , """"EventTime":""", """logged in""", """"UserName":""" ]
  Fields = [
  """"EventTime":"({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2})"""
  """"Message":"({additional_info}(User.*?@({src_ip}(((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\s*)?[^"]+)"""
  """"UserName":"((({domain}[^\\"]+)\\+)?({user}[\w\.\-]{1,40}\$?))"""
  """({operation}logged in)"""
  ]
  ParserVersion = "v1.0.0"


}
```