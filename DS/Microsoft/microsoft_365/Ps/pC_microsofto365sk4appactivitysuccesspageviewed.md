#### Parser Content
```Java
{
Name = "microsoft-o365-sk4-app-activity-success-pageviewed"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [ """destinationServiceName =Office 365""", """flexString1=PageViewed""" ]
Fields = [
  """\"CreationTime\\*\"+:\\*\s*\"+({time}[^\\\"]+)"""
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+\w)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wsuser=(({email_address}[^:@=\s]+?@[^=\s]+\.[^=\s]+?)|(anonymous|({user}[^:=\s]+?)))\s+(\w+=|$)"""
  """\"+UserId\"+:\"+({email_address}[^:@\s\"]+?@[^@\s\"]+\.[^@\s\"]+)\"+"""
  """\WfilePath=({object}[^=]+?)\s+(\w+=|$)"""
  """\WObjectUrl\":\"({object}[^\"]+?)\""""
  """\WsourceServiceName =({app}[^=]+?)\s+(\w+=|$)"""
  """\WflexString1=({operation}[^=]+?)\s+(\w+=|$)"""
  """\Wmsg=({additional_info}[^=]+?)\s+(\w+=|$)"""
  """\WdestinationServiceName =({event_subtype}[^=]+?)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```