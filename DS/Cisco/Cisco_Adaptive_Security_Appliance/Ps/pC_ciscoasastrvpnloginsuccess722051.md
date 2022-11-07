#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-success-722051
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Adaptive Security Appliance
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Conditions = [ """assigned to session""", """-722051""" ]
    Fields = [
      """Group <({realm}[^<>\s]+?)>""",
      """({time}\w+ \d+ (\d\d\d\d )?\d+:\d+:\d+)""",
      """[\s\t]+\d\d:\d\d:\d\d\s+({host}[\w.\-]+) : %ASA""",
      """({host}[^\s]+)\s+:\s+%FTD-""",
      """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
      """User[\s\t]+<(?![^\s]+@[^\s]+)({user}[^>]+)>[\s\t]+IP[\s\t]+<({src_ip}[^>]+)>[\s\t]+(?:IPv4[\s\t])?Address[\s\t]+<({src_translated_ip}[^>]+)>"""
      """User[\s\t]+<({email_address}[^>@]+@[^>@]+)>[\s\t]+IP[\s\t]+<({src_ip}[^>]+)>[\s\t]+(?:IPv4[\s\t])?Address[\s\t]+<({src_translated_ip}[^>]+)>""",
      """%ASA-({priority}\d+)-({event_code}\d+)""",
      """%FTD-({priority}\d+)-({event_code}\d+)"""
    ]
  

}
```