#### Parser Content
```Java
{
Name = "microsoft-o365-json-app-activity-success-operation"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """Workload""", """"LabelName"""", """"LabelId""", """Operation""" ]
Fields = [
  """\"*CreationTime\"*:\s*\"*({time}\d+-\d+-\d+T\d+:\d+:\d+)\"*"""
  """Workload\"*:\s*\"*({app}[^\"]+)\""""
  """\WsourceServiceName =({app}[^=]+?)\s+(\w+=|$)"""
  """ObjectId\"*:\s*\"*<?({object}[^\"]+?)>?\""""
  """Operation\"*:\s*\"*({operation}[^\"]+)\"*"""
  """UserId\"*:\s*\"*({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))\"*"""
  """Sender\"*:\s*\"*({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))\""""
  """Receivers\"*:\s*\[\"*({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|\+]+)"""
  """Receivers"*:\s*\[("*({recipients}[^",\]]+)"*|({=recipients}[^\]]+))\]"""
  """"UserType":\s*"*({user_type}[^\}"]+)\s*"*(,|\})"""
]
ParserVersion = "v1.0.0"


}
```