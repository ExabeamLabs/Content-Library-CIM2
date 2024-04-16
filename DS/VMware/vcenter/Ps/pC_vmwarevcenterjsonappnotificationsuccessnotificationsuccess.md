#### Parser Content
```Java
{
Name = vmware-vcenter-json-app-notification-success-notificationsuccess
  Vendor = VMware
  Product = vCenter
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
  Conditions = [ """"Message":""" , """"EventTime":""", """"UserName":""" ]
  Fields = [
    """exa_json_path=$.EventTime,exa_field_name=time"""
    """exa_json_path=$.Message,exa_regex=({additional_info}(User.*?@({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9]+:[A-Fa-f0-9:]+))\s*)?[^"]+?)"""
    """exa_json_path=$.UserName,exa_regex=((({domain}[^\\"]+)\\+)?({user}[\w\.\-]{1,40}\$?))"""
  ]
  ParserVersion = "v1.0.0"


}
```