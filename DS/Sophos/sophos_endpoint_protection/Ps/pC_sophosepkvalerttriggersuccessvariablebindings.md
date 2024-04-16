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
  """\sSource:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\s*\((({=src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({=src_port}\d+))?|({src_host}[\w\.-]+))\))?"""
  """:=\s*({additional_info}[^"]+?)\s+"({file_path}(({file_dir}.+)[\\\/])?({file_name}.+?))"\s+belongs to\s+({alert_type}.+?)\s+'({alert_name}.+?)'(\s*\(of type\s+({=alert_type}.+?)\))?"""
]
DupFields = [
  "file_path->malware_url"
]
ParserVersion = "v1.0.0"


}
```