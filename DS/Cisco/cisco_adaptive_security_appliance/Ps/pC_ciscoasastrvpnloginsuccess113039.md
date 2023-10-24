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
      """User\s+<((cn=({src_host}[^>,@]+))|({=src_host}[^.<@]+\.[^.>@]+\.[^>]*)|((({domain}[^\\\/>]+)[\\\/])?({user}[\w\.\-]{1,40}\$?)))(>|,[^>]+?dc=({=domain}[^>,]+))""",
      """User\s+<({email_address}[^@>]+@[^@>]+)>""",
      """ IP <({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))>""",
      """ Group\s+<({realm}.+?)>""",
      """\sGroup\s*<({group_name}[^>]+)>"""
      """\sUser\s*<({user}[\w\.\-]{1,40}\$?)>"""
    ]
    DupFields = [ "user->account"]
  

}
```