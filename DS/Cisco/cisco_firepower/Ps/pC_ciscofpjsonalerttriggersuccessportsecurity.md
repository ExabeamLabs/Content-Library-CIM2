#### Parser Content
```Java
{
Name = "cisco-fp-json-alert-trigger-success-portsecurity"
Vendor = "Cisco"
Product = "Cisco Firepower"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """PORT_SECURITY"""
  """PSECURE_VIOLATION: Security violation occurred"""
]
Fields = [
  """\w+\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?({host}[a-fA-F\d.:]+|[\w.\-]+)\s*\d+:"""
  """<\d+>\w+ \d+ \d+:\d+:\d+ ({host}[\w.\-]+)"""
  """({alert_type}PSECURE_VIOLATION):\s*({alert_name}[^,]+?),"""
  """caused by MAC address ({src_mac}[a-fA-F\d.:]+) on port ({src_interface}[^\.]+)"""
]
ParserVersion = "v1.0.0"


}
```