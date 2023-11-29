#### Parser Content
```Java
{
Name = "microsoft-o365-sk4-app-activity-success-pageviewed"
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [ """"Operation":"PageViewed"""", """"Workload":""" ]
Fields = [
  """\"CreationTime\\*\"+:\\*\s*\"+({time}[^\\\"]+)"""
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+\w)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F:]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wsuser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(anonymous|({user}[\w\.\-]{1,40}\$?)))\s+(\w+=|$)"""
  """\\?"+UserId\\?"+:\\?"+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\\?"+"""
  """\WfilePath=({object}[^=]+?)\s+(\w+=|$)"""
  """\WObjectUrl\":\"({object}[^\"]+?)\""""
  """\WsourceServiceName =({app}[^=]+?)\s+(\w+=|$)"""
  """\WflexString1=({operation}[^=]+?)\s+(\w+=|$)"""
  """\Wmsg=({additional_info}[^=]+?)\s+(\w+=|$)"""
  """destinationServiceName =({event_subtype}[^=]+?)\s+(\w+=|$)"""
  """"UserAgent":"({user_agent}[^"]+)""""
  """"BrowserName":"({browser}[^"]+)""""
  """"Platform":"(NotSpecified|({os}[^"]+))""""
  """"AuthenticationType":"({auth_type}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```