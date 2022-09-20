#### Parser Content
```Java
{
Name = sophos-ep-kv-alert-trigger-success-alertdetected
Vendor = Sophos
Product = Sophos Endpoint Protection
TimeFormat = "yyyy-MM-dd HH:mm:ss a"
Conditions = [
  """ has been detected"""
  """SOPHOS:"""
  """SNMP Trap"""
  """Variable Bindings"""
]
Fields = [
  """Address=({host}\S+)"""
  """({host}[\w\.-]+)\s+MSWinEventLog"""
  """\sReceived Time:({time}\d\d\d\d-\d\d-\d\d \d{1,2}:\d\d:\d\d (AM|PM|am|pm))"""
  """\sSource:({src_ip}[^\(\s]+)(\s*\(({src_host}[\w\.-]+)\))?"""
  """:=\s*({alert_type}.+?)\s+'({alert_name}.+?)'\s+has been detected in "({file_path}(({file_dir}.+)[\\\/])?({file_name}.+?))"\.(\s+({additional_info}.+?)\s+(\S+:=|$))?"""
  """:=\s*({additional_info}[^"]+?)\s+"({file_path}(({file_dir}.+)[\\\/])?({file_name}.+?))"\s+of\s+controlled application\s+'({alert_name}.+?)'\s*\(of type\s+({alert_type}.+?)\)\s+has been detected\."""
]
DupFields = [
  "file_path->malware_url"
]
ParserVersion = "v1.0.0"


}
```