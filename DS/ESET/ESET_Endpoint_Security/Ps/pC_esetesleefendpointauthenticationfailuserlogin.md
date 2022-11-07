#### Parser Content
```Java
{
Name = eset-es-leef-endpoint-authentication-fail-userlogin
Vendor = ESET
Product = ESET Endpoint Security
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
  """LEEF:"""
  """|ESET|RemoteAdministrator|"""
  """cat=ESET RA Audit Event"""
  """|Failed domain user login|"""
]
Fields = [
  """\Wcat=({category}[^=]+?)\s*(\w+=|$)"""
  """\Wsev=({alert_severity}\d+)"""
  """\WdevTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
  """\Wsrc=({src_ip}[a-fA-F:\d.]+)"""
  """\Waction=({operation}[^\s]+)\s"""
  """\Wresult=({action}[^=]+?)\s*(\w+=|$)"""
  """\WdeviceName =({host}[^\s]+)\s"""
  """\Wtarget=({object}[^\s]+)\s*"""
  """\Wdetail=({additional_info}[^.]+)."""
  """\Wuser '\w+\\({user}[^\s]+)'."""
  """(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\|({event_name}[^|]+)\|"""
  """({service_name}RemoteAdministrator)"""
  """\d+Z\s*({host}\w+)\s"""
]
ParserVersion = "v1.0.0"


}
```