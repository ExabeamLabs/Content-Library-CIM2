#### Parser Content
```Java
{
Name = "vectra-cd-cef-alert-trigger-success-vectranetworks"
Vendor = "Vectra"
Product = "Vectra Cognito Detect"
TimeFormat = "epoch"
Conditions = [
  """|Vectra Networks|X Series|"""
]
Fields = [
  """\Wrt=({time}\d{13})"""
  """\Wstart=({time}\d+)"""
  """\Wdvc=({host}[\w\-.]+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """CEF:([^|]*\|){4}({alert_type}[^|]+)"""
  """CEF:([^|]*\|){5}({alert_name}[^|]+)"""
  """\Wcat=({category}[^=]+?)\s*(\w+=|$)"""
  """\Wshost=({src_host}[\w\-.]+)\s"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\WexternalId=({alert_id}[^=]+?)\s*(\w+=|$)"""
  """\WflexNumber2=({confidence_level}[^=]+?)\s*(\w+=|$)"""
  """\WflexNumber1=({threat_id}[^=]+?)\s*(\w+=|$)"""
  """saccount=(\w+:)?(({email_address}[^@=]+?@[^.]+\.[^\s]+)|({account}[^=]+?))\s*\s*(\w+=|$)"""
  """\scs4=({additional_info}[^|]+?)\s\w+="""
]
ParserVersion = "v1.0.0"


}
```