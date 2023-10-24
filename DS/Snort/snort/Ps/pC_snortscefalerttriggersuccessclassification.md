#### Parser Content
```Java
{
Name = "snort-s-cef-alert-trigger-success-classification"
Vendor = "Snort"
Product = "Snort"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """[Classification:"""
  """[Priority:"""
  """PROTOCOL-"""
]
Fields = [
  """\}\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+->\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\[Classification:\s+({alert_type}[^\]]+)"""
  """\[Priority:\s+({alert_severity}[^\]]+)"""
  """PROTOCOL-({protocol}[^\s]+)\s+({alert_name}.+?)\s*\[Classification:"""
]
ParserVersion = "v1.0.0"


}
```