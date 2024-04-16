#### Parser Content
```Java
{
Name = trendmicro-ds-cef-database-login-fail-loginfailed
Vendor = Trend Micro
Product = Deep Security
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSSSSZ"
Conditions = [
  """CEF:"""
  """|Database Server - Microsoft SQL|"""
  """Login failed"""
]
Fields = [
  """\Wdvc=(|({host}.+?))(\s+\w+=|\s*$|\s*")"""
  """\Wshost=(|({src_host}.+?))(\s+\w+=|\s*$|\s*")"""
  """Login failed for user\s*'(({domain}[^']+?)\\+)?({user}[\w\.\-]{1,40}\$?)'"""
  """Reason:\s*({failure_reason}.+?)\s*\."""
]
ParserVersion = "v1.0.0"


}
```