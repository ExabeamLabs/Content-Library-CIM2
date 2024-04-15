#### Parser Content
```Java
{
Name = "tyco-ccure-kv-physical-location-access-card"
Vendor = "Tyco"
Product = "CCURE Building Management System"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  "MessageType=\"Card"
  "SecondaryObjectName =\""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)\"\s+(\w+=|$)"""
  """,\s*ServerName =\"({host}[^\"]+)"""
  """,\s*MessageType=\"({action}[^\"]+)"""
  """,\s*Name =\"({full_name}[^\"]+)\""""
  """,\s*Name =\"({last_name}[^\",]+)\s*,\s*({first_name}[^\"]+)\""""
  """,\s*CardNumber=\"({badge_id}\d+)"""
  """,\s*SecondaryObjectName =\"({location_door}[^\"]+)\""""
  """,\s*ServerUTC=\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """<Direction>\s*({direction}.+)\s*</Direction>"""
  """<Card>\s*({badge_id}\d+)\s*</Card>"""
  """<CHUID>\s*({badge_id}\d+)\s*</CHUID>"""
  """<PrimaryObjectName>\s*({last_name}[^,]+?),\s*({first_name}.*?)\s*</PrimaryObjectName>"""
  """<SecondaryObjectName>\s*({location_door}.+?)\s*</SecondaryObjectName>"""
  """<AdmitCode>\s*({result_reason}.+?)\s*</AdmitCode>"""
  """<RejectCode>\s*({result_reason}.+?)\s*</RejectCode>"""
]
ParserVersion = "v1.0.0"


}
```