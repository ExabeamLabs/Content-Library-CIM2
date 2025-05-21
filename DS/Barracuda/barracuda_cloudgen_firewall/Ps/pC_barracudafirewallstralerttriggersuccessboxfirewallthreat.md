#### Parser Content
```Java
{
Name = "barracuda-firewall-str-alert-trigger-success-boxfirewallthreat"
Vendor = "Barracuda"
Product = "Barracuda Cloudgen Firewall"
ParserVersion = "v1.0.0"
TimeFormat = "MMM dd HH:mm:ss"
Conditions = [
  """/box_Firewall_threat:"""
]
Fields = [
  """({time}\w+\s\d+\s\d\d:\d\d:\d\d)\s({host}[\w\_\.]+)\s\w+\/({event_name}box_Firewall_threat):\s*[\w\-:]+\s*({alert_severity}[^\s]+)\s"""
  """\/box_Firewall_threat:.+?firewall:\s*({additional_info}[^\|]+?)\s*\|"""
  """\/box_Firewall_threat:[^\|]+\|\[({alert_name}[^\]]+)"""
  """\/box_Firewall_threat:[^\|]+?firewall:\s+[^:]+:\s+\w+\s+({protocol}[^\s]+)"""
  """\/box_Firewall_threat:[^\|]+?firewall:\s+[^:]+:\s+\w+\s+([^\s]+)\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """\/box_Firewall_threat:[^\|]+?firewall:\s+[^:]+:\s+\w+\s+([^\s]+)\s(((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})) ->\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))"""
]


}
```