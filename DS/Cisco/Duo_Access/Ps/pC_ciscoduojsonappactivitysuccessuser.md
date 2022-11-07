#### Parser Content
```Java
{
Name = cisco-duo-json-app-activity-success-user
Vendor = Cisco
Product = Duo Access
TimeFormat = "epoch_sec"
Conditions = [
  """"object":"""
  """"timestamp":"""
  """"event_time":"""
  """"username":"""
]
Fields = [
  """object":"({object}[^"]+)""""
  """timestamp":({time}\d{10})"""
  """username":"({user}[^"]+)""""
  """action":"({operation}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```