#### Parser Content
```Java
{
Name = "microsoft-evnps-kv-radius-traffic-fail-6273"
Vendor = "Microsoft"
Product = "Event Viewer - NPS"
TimeFormat = "epoch_sec"
Conditions = [
  """EventIDCode=6273"""
  """Network Policy Server denied access to a user"""
]
Fields = [
  """TimeGenerated=({time}\d{10})"""
  """Message=\s*({event_name}.+?)\.\s+"""
  """EventIDCode=({event_code}\d+)"""
 """Computer=({host}[\w\-.]+)"""
 """User=(|({user}[^\s]+))"""
  """Domain=(|({domain}[^\s]+))"""
  """User:.+?\sAccount Name:\s*(|(?:({user_type}host)/)?(({domain}[^\\\/]+?)[\\\/]+)?({user}.+?))\s*Account Domain:\s*(|({=domain}.+?))\s*Fully Qualified Account Name:(|(({=domain}[^\\\/]+?)[\\\/]+)?({=user}.+?))"""
  """\sCalled Station Identifier:\s*(-|({dest_mac}\w{2}-\w{2}-\w{2}-\w{2}-\w{2}-\w{2})|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
  """\sCalling Station Identifier:\s*(-|({src_mac}\w{2}-\w{2}-\w{2}-\w{2}-\w{2}-\w{2})|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
  """\sNAS IPv(4|6) Address:\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sNAS Identifier:\s*(-|({location}.+?))\s*NAS Port-Type:"""
  """({result}denied)"""
]
ParserVersion = "v1.0.0"


}
```