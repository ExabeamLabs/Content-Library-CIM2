#### Parser Content
```Java
{
Name = sophos-ep-kv-alert-trigger-success-variablebindings
Vendor = Sophos
Product = Sophos Endpoint Protection
TimeFormat = "yyyy-MM-dd HH:mm:ss a"
Conditions = [
  """ belongs to """
  """SOPHOS:"""
  """SNMP Trap"""
  """Variable Bindings"""
]
Fields = [
  """Address=({host}\S+)"""
  """({host}[\w\.-]+)\s+MSWinEventLog"""
  """\sReceived Time:({time}\d\d\d\d-\d\d-\d\d \d{1,2}:\d\d:\d\d (AM|PM|am|pm))"""
  """\sSource:({src_ip}[^\(\s]+)(\s*\(({src_host}[\w\.-]+)\))?"""
  """:=\s*({additional_info}[^"]+?)\s+"({file_path}(({file_dir}.+)[\\\/])?({file_name}.+?))"\s+belongs to\s+({alert_type}.+?)\s+'({alert_name}.+?)'(\s*\(of type\s+({=alert_type}.+?)\))?"""
]
DupFields = [
  "file_path->malware_url"
]
ParserVersion = "v1.0.0"


}
```