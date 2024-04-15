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
  """UserId\"*:\s*\"*({email_address}[^@]+@({email_domain}[^\"]+))\"*"""
  """Sender\"*:\s*\"*({src_email_address}[^\"]+)\""""
  """Receivers\"*:\s*\[\"*({dest_email_address}[^"\]]+)"""
]
DupFields = [
  "src_email_address->email_address"
  "dest_email_address->recipients"
]
ParserVersion = "v1.0.0"


}
```