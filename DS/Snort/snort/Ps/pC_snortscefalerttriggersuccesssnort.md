#### Parser Content
```Java
{
Name = "snort-s-cef-alert-trigger-success-snort"
Vendor = "Snort"
Product = "Snort"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """CEF:"""
  """|snort|"""
  """proto="""
]
Fields = [
  """:\d\d:\d\d\s({host}[\w\-.]+)"""
  """CEF:([^\|]*\|){3}\d+\.\d+:\d+:({alert_id}\d+)"""
  """CEF:([^\|]*\|){4}({alert_name}[^|]+)"""
  """CEF:([^\|]*\|){5}({alert_severity}\d+)"""
  """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """spt=({src_port}\d+)"""
  """dpt=({dest_port}\d+)"""
  """proto=({protocol}[^=]+?)\s*(\w+=|$)"""
]
DupFields = [
  "alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```