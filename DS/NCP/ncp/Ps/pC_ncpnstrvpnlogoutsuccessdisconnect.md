#### Parser Content
```Java
{
Name = ncp-n-str-vpn-logout-success-disconnect
  Vendor = NCP
  Product = NCP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ disconnect """, """ : incoming : """, """ConTime=""" ]
  Fields = [
    """<.+?>\w+ \d+ \d\d:\d\d:\d\d ({host}\S+)\s+disconnect""",
    """incoming\s*:\s*({user}[\w\.\-]{1,40}\$?)(@({domain}[^\s@]+)\s*:)"""
  ]
  ParserVersion = "v1.0.0"


}
```