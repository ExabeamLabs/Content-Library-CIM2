#### Parser Content
```Java
{
Name = cisco-fp-str-app-authentication-113009
  Vendor = Cisco
  Product = Cisco Network Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ 
  """-113009"""
  """%FTD-"""
  ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """server\s*=\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """-113009:\s+({event_name}AAA retrieved default group policy)"""
    """user\s*=\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@,\s:]+))?"""
  ]


}
```