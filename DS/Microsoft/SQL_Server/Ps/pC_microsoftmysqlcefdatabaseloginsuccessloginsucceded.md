#### Parser Content
```Java
{
Name = microsoft-mysql-cef-database-login-success-loginsucceded
Vendor = "Microsoft"
Product = "SQL Server"
TimeFormat = "MMM dd yyyy HH:mm:ss z"
Conditions = [
  """CEF:"""
  """|LOGbinder|SQL|"""
  """|24001|Login succeeded"""
]
Fields = [
  """({host}[\w.\-]+)\s+CEF:"""
  """\Wrt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d \w+)"""
  """\W(d|s)user=(n/a|(({domain}[^=\\\/]+)[\\\/]+)?({user}[^=\\\/]+?))(\s+\w+=|\s*$)"""
  """\WdeviceExternalId=(|({dest_host}.+?))(\s+\w+=|\s*$)"""
  """network protocol:\s*({protocol}[^;]+)"""
  """<address>({src_ip}[a-fA-F\d.:]+)</address>"""
]
ParserVersion = "v1.0.0"


}
```