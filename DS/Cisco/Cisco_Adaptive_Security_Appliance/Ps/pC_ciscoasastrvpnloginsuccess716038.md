#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-success-716038
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Adaptive Security Appliance
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Conditions = [ """WebVPN""", """Authentication: successful""" , """-716038""" ]
    Fields = [
      """({time}\w+ \d+ \d\d\d\d \d+:\d+:\d+)""",
      """User\s+<({user}[^>]+)>""",
      """IP\s+<({src_ip}[^>]+)>""",
      """%ASA-({priority}\d+)-({event_code}\d+)""",
      """Group\s*<({group_name}.*?)>"""
    ]
    DupFields = [ "group_name->realm" ]
  

}
```