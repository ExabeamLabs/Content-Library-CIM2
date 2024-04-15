#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-login-680"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """|Snare|"""
  """|Security:680|"""
]
Fields = [
  """({event_code}680)"""
  """({event_name}Logon attempt)"""
  """\srt=({time}\d+)"""
  """ahost=({host}[^\s]+)"""
  """suser=({user}.+?)\s+\w+="""
  """dhost=({dest_host}.+?)\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```