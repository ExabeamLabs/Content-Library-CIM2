#### Parser Content
```Java
{
Name = cisco-ac-str-vpn-login-success-722055
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = AnyConnect
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","MMM dd HH:mm:ss"]
    Conditions = [ """Client Type: Cisco AnyConnect VPN Agent""", """-722055""", """%FTD-""" ]
    Fields = [
      """\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD-""",
      """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
      """%FTD-({priority}\d+)-({event_code}\d+)""",
      """({time}\w+ \d+ (\d\d\d\d )\d+:\d+:\d+)""",
      """({time}\w+\s+\d+\s+\d\d:\d\d:\d\d)""",
      """User\s+<(?![^\s]+@[^\s]+)({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@[^>]+)?>""",
      """User\s+<({full_name}[^,@]+\s\w+)>""",
      """User\s+<({email_address}[^@>]+@[^@>]+)>""",
      """ IP <({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))>""",
      """Group\s+<({realm}.+?)>""",
      """Cisco AnyConnect VPN Agent for ({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(X|x)11|(W|w)indows|(L|l)inux|(M|m)acintosh|(D|d)arwin)"""
   ]
  

}
```