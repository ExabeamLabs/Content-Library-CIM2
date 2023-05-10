#### Parser Content
```Java
{
Name = cisco-ac-str-vpn-login-success-722055
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = AnyConnect
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Conditions = [ """Client Type: Cisco AnyConnect VPN Agent""", """-722055""", """%FTD-""" ]
    Fields = [
      """({host}[^\s]+)\s+:\s+%FTD-""",
      """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
      """%FTD-({priority}\d+)-({event_code}\d+)""",
      """({time}\w+ \d+ (\d\d\d\d )?\d+:\d+:\d+)""",
      """({time}\d+ \w+ \d+\d+:\d+:\d+)""",
      """User\s+<(?![^\s]+@[^\s]+)({user}[^@>\s]+)(?:@[^>]+)?>""",
      """User\s+<({full_name}[^,@]+\s\w+)>""",
      """User\s+<({email_address}[^@>]+@[^@>]+)>""",
      """ IP <({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})>""",
      """Group\s+<({realm}.+?)>""",
      """Cisco AnyConnect VPN Agent for ({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(X|x)11|(W|w)indows|(L|l)inux|(M|m)acintosh|(D|d)arwin)"""
   ]
  

}
```