#### Parser Content
```Java
{
Name = kaspersky-endpointsecurity-kv-alert-trigger-success-eventlog
Vendor = Kaspersky
Product = Kaspersky Endpoint Security for Business
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
  """Kaspersky Event Log"""
  """Result\Name:"""
]
Fields = [
  """ComputerName =({host}[\w.\-]+)"""
  """Message=({src_host}.+?)\s*\["""
  """User:\s+({domain}[^\\]*)\\({user}.+?)\s*\("""
  """Object:\s+({malware_url}.+?)\s*(Result|Object)"""
  """Result\Name:\s*({alert_type}.+?)\s*Result"""
  """Result\Type:\s*({alert_type}.+?)\s*Result"""
  """Result\Name:\s*({alert_name}.+?)\s*Result"""
  """Result\Threat level:\s*({alert_severity}.+?)\s*Result"""
]
ParserVersion = "v1.0.0"


}
```