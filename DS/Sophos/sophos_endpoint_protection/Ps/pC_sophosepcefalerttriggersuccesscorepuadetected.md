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
  """source_info_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sid=({alert_id}[^\s]+)\s"""
  """dhost=({dest_host}[^$\s]+?)\s*$"""
  """Event::Endpoint::CorePuaDetection\|[^\|]+\|({alert_severity}\d+)\|"""
  """Event::Endpoint::CorePuaDetection\|({additional_info}[^\|]+)\|"""
  """threat=({alert_name}[^=]+?)\s\w+="""
  """({alert_type}Event::Endpoint::CorePuaDetection)"""
  """suser=(({full_name}({last_name}[^,]+),\s({first_name}[^=\(]+?)\s\([^\)]+\))|(({domain}[^\\\s=]+)\\+)({user}[\w\.\-]{1,40}\$?)|({email_address}[^@]+@[^@\s=]+?))\s\w+="""
  """PUA detected: '[^']+' at '({malware_url}[^']+)'"""
]
ParserVersion = "v1.0.0"


}
```