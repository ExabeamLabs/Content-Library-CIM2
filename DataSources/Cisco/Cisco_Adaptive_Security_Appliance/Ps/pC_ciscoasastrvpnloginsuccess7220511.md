#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-success-722051-1
    Vendor = Cisco
    Product = Cisco Adaptive Security Appliance
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Conditions = [ """-iPhone> IP""", """-722051""" ]
    Fields = [
      """({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d)""",
      """User[\s\t]+<({user}.+?)-({src_host}[\w]+-iPhone)>[\s\t]+IP[\s\t]+<({src_ip}[^>]+)>[\s\t]+(?:IPv4[\s\t])?Address[\s\t]+<({src_translated_ip}[^>]+)>"""
    ]
        ParserVersion = "v1.0.0"
  

}
```