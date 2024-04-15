#### Parser Content
```Java
{
Name = "microsoft-exchange-sk4-app-activity-success-harddelete"
Vendor = "Microsoft"
Product = "Microsoft Exchange"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [  """destinationServiceName =Office 365""", """flexString1=HardDelete """, """request=Success""" ]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+\w)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wsuser=({user}.+?)\s+(\w+=|$)"""
  """\Wfname=({object}.+?)\s+(\w+=|$)"""
  """\WsourceServiceName =({app}.+?)\s+(\w+=|$)"""
  """\WflexString1=({operation}.+?)\s+(\w+=|$)"""
  """\Wmsg=({additional_info}.+?)\s+(\w+=|$)"""
  """\WdestinationServiceName =({event_subtype}.+?)\s+(\w+=|$)"""
]
DupFields = [
  "user->email_address"
]
ParserVersion = "v1.0.0"


}
```