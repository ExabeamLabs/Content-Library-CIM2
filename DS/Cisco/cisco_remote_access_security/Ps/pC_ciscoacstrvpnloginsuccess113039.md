#### Parser Content
```Java
{
Name = cisco-ac-str-vpn-login-success-113039
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Remote Access Security
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","MMM dd HH:mm:ss"]
    Conditions = [ """AnyConnect parent session started.""", """-113039""", """%FTD-""" ]
    Fields = [
      """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD-""",
      """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
      """%FTD-({priority}\d+)-({event_code}\d+)""",
      """({time}\w+ \d+ (\d\d\d\d )\d+:\d+:\d+)""",
      """({time}\w+\s+\d+\s+\d\d:\d\d:\d\d)""",
      """User\s+<(?![^\s]+@[^\s]+)({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@[^>]+)?>""",
      """User\s+<({full_name}[^,@]+\s\w+)>""",
      """User\s+<({email_address}[^@>]+@[^@>]+)>""",
      """IP <({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))>""",
      """Group\s+<({realm}.+?)>"""
    ]
  

}
```