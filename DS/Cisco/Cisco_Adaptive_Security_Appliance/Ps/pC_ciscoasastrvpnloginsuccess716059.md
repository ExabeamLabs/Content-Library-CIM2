#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-success-716059
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Adaptive Security Appliance
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Conditions = [ """AnyConnect session resumed connection from IP""" , """-716059""" ]
    Fields = [
      """({time}\w+ \d+ \d\d\d\d \d+:\d+:\d+)""",
      """({host}[^\s]+)\s+:\s+%FTD-""",
      """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
      """User\s+<({user}[^>]+)>""",
      """IP\s+<({src_ip}[^>]+)>""",
      """%ASA-({priority}\d+)-({event_code}\d+)""",
      """%FTD-({priority}\d+)-({event_code}\d+)""",
      """Group\s*<({group_name}.*?)>"""
     ]
     DupFields = [ "group_name->realm" ]
  

}
```