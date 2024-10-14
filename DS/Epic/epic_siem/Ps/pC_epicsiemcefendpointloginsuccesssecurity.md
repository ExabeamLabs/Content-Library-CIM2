#### Parser Content
```Java
{
Name = "epic-siem-cef-endpoint-login-success-security"
Vendor = "Epic"
Product = "Epic SIEM"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """CEF:"""
  """|Epic|Security-SIEM|"""
  """|AUTHENTICATION|"""
]
Fields = [
  """CEF:([^\|]*\|){5}({operation}[^\|]+)"""
  """({host}[\w\-.]+)\s+CEF:"""
  """LOGINLDAPID=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """workstationID=({dest_host}[\w\-.]+)"""
  """shost=({src_host}[\w\-.]+)"""
]
ParserVersion = "v1.0.0"


}
```