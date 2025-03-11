#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-success-716038
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Network Security
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Conditions = [ """WebVPN""", """Authentication: successful""" , """-716038""", """%ASA-""" ]
    Fields = [
      """({time}\w+ \d+ \d\d\d\d \d+:\d+:\d+)""",
      """User\s*<(({email_address}[^@>]+@[^>\.]+\.[^>]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))>""",
      """IP\s+<({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?>""",
      """%ASA-({priority}\d+)-({event_code}\d+)""",
      """Group\s*<({group_name}.*?)>"""
    ]
    DupFields = [ "group_name->realm" ]
  

}
```