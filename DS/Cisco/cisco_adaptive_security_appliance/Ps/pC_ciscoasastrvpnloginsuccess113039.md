#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-success-113039
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Adaptive Security Appliance
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Conditions = [ """-113039""", """%ASA-""" ]
    Fields = [
      """%ASA-({priority}\d+)-({event_code}\d+)""",
      """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
      """User\s+<((cn=({src_host}[^>,@]+))|({=src_host}[^.<@]+\.[^.>@]+\.[^>]*)|((({domain}[^\\\/>]+)[\\\/])?({user}[^@>]+?)))(>|,[^>]+?dc=({=domain}[^>,]+))""",
      """User\s+<({email_address}[^@>]+@[^@>]+)>""",
      """ IP <({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})>""",
      """ Group\s+<({realm}.+?)>"""
    ]
    DupFields = [ "user->account"]
  

}
```