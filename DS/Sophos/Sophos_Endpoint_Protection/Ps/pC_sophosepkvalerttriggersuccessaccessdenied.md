#### Parser Content
```Java
{
Name = sophos-ep-kv-alert-trigger-success-accessdenied
Vendor = Sophos
Product = Sophos Endpoint Protection
TimeFormat = "yyyy-MM-dd HH:mm:ss a"
Conditions = [
  """On-access scanner has denied access to location """
  """SOPHOS:"""
  """SNMP Trap"""
  """Variable Bindings"""
]
Fields = [
  """Address=({host}\S+)"""
  """({host}[\w\.-]+)\s+MSWinEventLog"""
  """\sReceived Time:({time}\d\d\d\d-\d\d-\d\d \d{1,2}:\d\d:\d\d (AM|PM|am|pm))"""
  """\sSource:({src_ip}[^\(\s]+)(\s*\(({src_host}[\w\.-]+)\))?"""
  """:=\s*On-access scanner has denied access to location "({file_path}(({file_dir}.+)[\\\/])?({file_name}.+?))"\s+(for user\s+(({domain}.+?)\\)?({user}.+?)\s+(\S+=|$))?"""
  """({access}access)"""
  """({alert_name}denied access)"""
]
DupFields = [
  "alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```