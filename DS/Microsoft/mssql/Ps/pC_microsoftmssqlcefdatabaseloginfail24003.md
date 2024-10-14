#### Parser Content
```Java
{
Name = microsoft-mssql-cef-database-login-fail-24003
Vendor = "Microsoft"
Product = "MSSQL"
TimeFormat = "MMM dd yyyy HH:mm:ss z"
Conditions = [
  """CEF:"""
  """|LOGbinder|SQL|"""
  """|24003|Login failed|"""
]
Fields = [
  """({host}[\w.\-]+)\s+CEF:"""
  """\Wrt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d \w+)"""
  """\Wsuser=(n/a|(({domain}[^=\\\/]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
  """\WdeviceExternalId=(|({dest_host}[\w\-.]+?))(\s+\w+=|\s*$)"""
  """\Wcs1=({result_reason}[^;\.]+)"""
  """Reason:\s*({result_reason}[^;\.]+)"""
  """<address>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?</address>"""
  """CLIENT:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```