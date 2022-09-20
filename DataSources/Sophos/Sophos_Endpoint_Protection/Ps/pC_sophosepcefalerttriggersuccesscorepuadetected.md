#### Parser Content
```Java
{
Name = sophos-ep-cef-alert-trigger-success-corepuadetected
Vendor = Sophos
Product = Sophos Endpoint Protection
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """CEF:"""
  """Event::Endpoint::CorePuaDetection"""
  """PUA detected:"""
]
Fields = [
  """rt=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)"""
  """source_info_ip=({src_ip}[a-fA-F\d:.]+)"""
  """\sid=({alert_id}[^\s]+)\s"""
  """dhost=({dest_host}[^$\s]+?)\s*$"""
  """Event::Endpoint::CorePuaDetection\|[^\|]+\|({alert_severity}\d+)\|"""
  """Event::Endpoint::CorePuaDetection\|({additional_info}[^\|]+)\|"""
  """threat=({alert_name}[^=]+?)\s\w+="""
  """({alert_type}Event::Endpoint::CorePuaDetection)"""
  """suser=(({full_name}({last_name}[^,]+),\s({first_name}[^=\(]+?)\s\([^\)]+\))|(({domain}[^\\\s=]+)\\+)({user}[^\s=]+?)|({email_address}[^@]+@[^@\s=]+?))\s\w+="""
  """PUA detected: '[^']+' at '({malware_url}[^']+)'"""
]
ParserVersion = "v1.0.0"


}
```