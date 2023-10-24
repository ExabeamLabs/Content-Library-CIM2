#### Parser Content
```Java
{
Name = trendmicro-officescan-kv-alert-trigger-success-transmissiondetected
Vendor = Trend Micro
Product = OfficeScan
TimeFormat = "MM/dd/yyyy HH:mm:ss"
Conditions = [
  """Digital asset transmission detected"""
  """ Template:"""
]
Fields = [
  """Date\/Time:\s*({time}\d+\/\d+\/\d\d\d\d \d\d:\d\d:\d\d)"""
  """Endpoint:\s*({src_host}[^\s]+)"""
  """User:\s*({user}[\w\.\-]{1,40}\$?)\s+\w+:"""
  """Domain:\s*({domain}[^\\]+)\\"""
  """Channel:\s*({alert_type}.+?)\s+\w+:"""
  """Channel:\s*({protocol}.+?)\s+\w+:"""
  """Rule:\s*({alert_name}.+?)\s*$"""
]
ParserVersion = "v1.0.0"


}
```