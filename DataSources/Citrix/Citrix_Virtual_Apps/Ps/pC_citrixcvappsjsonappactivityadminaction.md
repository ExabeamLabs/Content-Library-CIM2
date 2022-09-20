#### Parser Content
```Java
{
Name = citrix-cvapps-json-app-activity-adminaction
  ParserVersion = v1.0.0
  Vendor = Citrix
  Product = Citrix Virtual Apps
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"event":"admin-action"""", """"system":"Citrix-XenApp"""", """"adminmachineip":"""", """"adminaccountname":"""" ]
  Fields = [
    """"starttime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""",
    """"username":"(({email_address}[^@"]+@[^\."]+\.[^"]+)|(({domain}[^\\"]+)\\+)?({user}[^"]+))"""",
    """"text":"({additional_info}[^"]+)",""",
    """"adminaccountname":"(({account_domain}[^\\"]+)\\+)?({account_name}[^"]+)",""",
    """({event_name}admin-action)"""
  ]


}
```