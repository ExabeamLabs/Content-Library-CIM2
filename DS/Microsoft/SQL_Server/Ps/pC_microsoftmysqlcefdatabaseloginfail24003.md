#### Parser Content
```Java
{
Name = microsoft-mysql-cef-database-login-fail-24003
Vendor = "Microsoft"
Product = "SQL Server"
TimeFormat = "MMM dd yyyy HH:mm:ss z"
Conditions = [
  """CEF:"""
  """|LOGbinder|SQL|"""
  """|24003|Login failed|"""
]
Fields = [
  """({host}[\w.\-]+)\s+CEF:"""
  """\Wrt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d \w+)"""
  """\Wsuser=(n/a|(({domain}[^=\\\/]+)[\\\/]+)?({user}[^=\\\/]+?))(\s+\w+=|\s*$)"""
  """\WdeviceExternalId=(|({dest_host}.+?))(\s+\w+=|\s*$)"""
  """\Wcs1=({failure_reason}[^;\.]+)"""
  """Reason:\s*({failure_reason}[^;\.]+)"""
  """<address>({src_ip}[a-fA-F\d.:]+)</address>"""
  """CLIENT:\s*({src_ip}[a-fA-F\d.:]+)"""
]
ParserVersion = "v1.0.0"


}
```