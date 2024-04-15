#### Parser Content
```Java
{
Name = "snort-s-str-alert-trigger-success-classification"
Vendor = "Snort"
Product = "Snort"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """snort:"""
  """Classification:"""
]
Fields = [
  """snort:\s*\[({alert_id}[^\]]+?)\]\s*({alert_name}[^\[]+?)\s*\[Classification"""
  """({alert_name}snort: \d+:\d+:\d+)"""
  """Classification: ({alert_type}[^\]]+?)\]?\s*\[?Priority: ({alert_severity}\d+)"""
  """snort: \d+:\d+:\d+ ({additional_info}[^:]+?) Classification:"""
  """(<({src_interface}[^<>]*?)>)? \{({protocol}\w+)\} ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\:({src_port}\d+)"""
  """(<({src_interface}[^<>]*?)>)? \{({protocol}\w+)\} ({src_port}\d+):({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({=src_port}\d+))?"""
  """-> ({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\:({dest_port}\d+)"""
  """-> ({dest_port}\d+):({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({=dest_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```