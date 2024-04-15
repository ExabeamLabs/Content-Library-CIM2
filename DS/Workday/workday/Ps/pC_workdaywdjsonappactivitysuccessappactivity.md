#### Parser Content
```Java
{
Name = "workday-wd-json-app-activity-success-appactivity"
Vendor = "Workday"
Product = "Workday"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """:"workday""""
  """"wd_systemaccount":"""
  """"wd_ipaddress":"""
  """"wd_activitycategory":"""
  """"wd_task":"""
]
Fields = [
  """timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
  """hostname":"({host}[^"]+?)""""
  """device_product":"({app}[^"]+?)""""
  """wd_systemaccount":"({domain}[^\/]+?)\s\/\s({full_name}[^"]+?)(\son behalf of\s[^"]+)?""""
  """wd_task":"({operation}[^"]+?)""""
  """wd_target":"({object}[^"]+?)""""
  """wd_useragent":"({user_agent}[^"]+?)""""
  """wd_ipaddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
]
ParserVersion = "v1.0.0"


}
```