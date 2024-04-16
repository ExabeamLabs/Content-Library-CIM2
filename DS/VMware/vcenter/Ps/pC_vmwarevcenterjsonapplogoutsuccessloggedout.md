#### Parser Content
```Java
{
Name = vmware-vcenter-json-app-logout-success-loggedout
  Vendor = VMware
  Product = vCenter
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  ExtractionType = json
  Conditions = [ """"Message":""" , """"EventTime":""", """logged out""", """"UserName":""" ]
  Fields = [
  """exa_json_path=$.EventTime,exa_field_name=time"""
  """exa_json_path=$.Message,exa_regex=({additional_info}(User.*?@({src_ip}(((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))\s*)?[^"]+)"""
  """exa_json_path=$.UserName,exa_regex=((({domain}[^\\"]+)\\+)?({user}[\w\.\-]{1,40}\$?))"""
  """exa_regex=({operation}logged out)"""
  ]
  ParserVersion = "v1.0.0"


}
```