#### Parser Content
```Java
{
Name = "cisco-fp-kv-alert-trigger-success-interfaceingress"
Vendor = "Cisco"
Product = Cisco Network Security
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ SFIMS: ["""
  """, Interface Ingress: """
  """, Security Zone Egress: """
]
Fields = [
  """({host}[\w\.-]+)\s+SFIMS:"""
  """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
  """Protocol:\s*(Unknown|({protocol}[^,]+))"""
  """"({alert_name}[^"]+)"\s*\[Classification:\s*(Unknown|({alert_type}[^\]]+))"""
  """User:\s*(Unknown|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """Interface Ingress:\s*(Unknown|({ingress_interface}[^,]+))"""
  """Interface Egress:\s*(Unknown|({egress_interface}[^,]+))"""
  """Security Zone Ingress:\s*(Unknown|({ingress_zone}[^,]+))"""
  """Security Zone Egress:\s*(Unknown|({egress_zone}[^,]+))"""
  """(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))(:({src_port}\d+))?\s*->\s*(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))(:({dest_port}\d+))?"""
  """\[Priority:\s*({alert_severity}\d+)\]"""
]
ParserVersion = "v1.0.0"


}
```