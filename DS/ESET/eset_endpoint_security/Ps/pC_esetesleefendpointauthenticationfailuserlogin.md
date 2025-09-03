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
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Waction=({operation}[^\s]+)\s"""
  """\Wresult=({action}[^=]+?)\s*(\w+=|$)"""
  """\WdeviceName =({host}[^\s]+)\s"""
  """\Wtarget=({object}[^\s]+)\s*"""
  """\Wdetail=({additional_info}[^.]+)."""
  """\Wuser '\w+\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)'."""
  """(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\|({event_name}[^|]+)\|"""
  """({service_name}RemoteAdministrator)"""
  """\d+Z\s*({host}\w+)\s"""
]
ParserVersion = "v1.0.0"


}
```