#### Parser Content
```Java
{
Name = safend-dps-kv-peripheral-storage-insert-success-allowed
Vendor = "Safend"
Product = "Data Protection Suite (DPS)"
TimeFormat = "MM dd yyyy HH:mm:ss"
Conditions = [
"""[Safend Data Protection]"""
"""Action: Read"""
]
Fields = [
"""Client GMT:\s+({time}\d+/\d+/\d\d\d\d \d\d:\d\d:\d\d (AM|PM|am|pm))"""
"""Action:\s*({operation}[^,]+?)\s*$"""
"""User:\s*({user}[^@,\s]+)(@({domain}[^@,.\s]+))?"""
"""User:\s*({email_address}[^,\s]+)"""
"""Computer:\s*({host}[^,]+)"""
"""Operating System:\s*({os}[^,]+)"""
"""Device Type:\s*({device_type}[^,]+)"""
"""Device Info:\s*({device_type}[^,]+),"""
"""Distinct ID:\s*(|({device_id}[^,]+)),"""
"""({operation_details}Policy:\s*[^,]+)"""
"""File Name:\s*({file_path}[^,]+)"""
"""File Name:\s*.+?\\({file_name}[^\\,]+),"""
"""File Name:[^,]+\.({file_ext}\w+),"""
"""File Type:\s*({file_ext}\w+)"""
"""File Size:\s*({bytes}\d+)"""
 """[Safend Data Protection]"""
  """Action: Allowed,"""
]
Fields = [
  """Action:\s*({operation}[^,]+)"""
  """User:\s*({email_address}[^,]+)"""
  """Computer:\s*({host}[^,]+)"""
  """Operating System:\s*({os}[^,]+)"""
  """Device Type:\s*({device_type}[^,]+)"""
  """Distinct ID:\s*(|({device_id}[^,]+)),"""
  """Policy:\s*({operation_details}[^,]+)"""
]
ParserVersion = "v1.0.0"


}
```