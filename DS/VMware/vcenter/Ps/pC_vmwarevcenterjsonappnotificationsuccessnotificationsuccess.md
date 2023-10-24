#### Parser Content
```Java
{
Name = vmware-vcenter-json-app-notification-success-notificationsuccess
  Vendor = VMware
  Product = vCenter
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"Message":""" , """"EventTime":""", """"UserName":""" ]
  Fields = [
  """"EventTime":"({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2})"""
  """"Message":"\s*({additional_info}(User.*?@({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9]+:[A-Fa-f0-9:]+))\s*)?[^"]+?)""""
  """"UserName":"((({domain}[^\\"]+)\\+)?({user}[\w\.\-]{1,40}\$?))"""
  ]
  ParserVersion = "v1.0.0"


}
```