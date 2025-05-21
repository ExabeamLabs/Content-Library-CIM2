#### Parser Content
```Java
{
Name = "cisco-fp-kv-alert-trigger-success-acpolicy"
Vendor = "Cisco"
Product = Cisco Network Security
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """IngressInterface:"""
  """ACPolicy:"""
  """IntrusionPolicy:"""
  """-430001:"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)\s*({host}[\w.\-]+)?"""
  """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
  """\sSrcIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sDstIP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sSrcPort:\s*({src_port}\d+)"""
  """\sDstPort:\s*({dest_port}\d+)"""
  """\sProtocol:\s*({protocol}[^,]+?)(,|\s*$)"""
  """\sUser:\s*(Unknown|No Authentication Required|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(,|\s*$)"""
  """\sIngressInterface:\s*({ingress_interface}[^,]+?)(,|\s*$)"""
  """\sEgressInterface:\s*({egress_interface}[^,]+?)(,|\s*$)"""
  """\sClassification:\s*({alert_type}[^,]+?)(,|\s*$)"""
  """\sIntrusionPolicy:\s*({alert_name}[^,]+?)(,|\s*$)"""
  """\sMessage:\s*({alert_name}[^,]+?)(,|\s*$)"""
  """\sPriority:\s*({alert_severity}\d+)"""
]
ParserVersion = "v1.0.0"


}
```