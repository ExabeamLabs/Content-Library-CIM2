#### Parser Content
```Java
{
Name = "procad-p-json-app-activity-appactivity"
Vendor = "Procad"
Product = "Pro.File DMS"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"pdmobjectsubtypename":""""
  """"pdmobjecttypename":""""
]
Fields = [
  """autodatetime":"({time}[^"]+)"""
  """pdmobjecttypename":"({resource}[^"]+)"""
  """pdmusername":"({user}[^"]+)"""
  """pdmserverlocation":"({host}[^"]+)"""
  """pdmobjectsubtypename":"({object}[^"]+)"""
  """pdmobjectactionname":"({operation}[^"]+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```