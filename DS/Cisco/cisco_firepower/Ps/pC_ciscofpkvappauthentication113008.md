#### Parser Content
```Java
{
Name = cisco-fp-kv-app-authentication-113008
  Vendor = Cisco
  Product = Cisco Firepower
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","MMM dd yyyy HH:mm:ss"]
  Conditions = [ 
  """-113008"""
  """%FTD-""" 
  ]
  Fields = [
    """({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)\s[\w\-\.]+\s*:\s*%FTD""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+Z)\s({host}[^\s]+)""",
    """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
    """%FTD-({priority}\d+)-({event_code}\d+)"""
    """-113008:\s+({event_name}AAA transaction status ACCEPT)"""
    """ user\s*=?\s*(({domain}[^\s\/\\]+)[\\\/])?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@({=domain}[^\s]+))?"""
  ]


}
```