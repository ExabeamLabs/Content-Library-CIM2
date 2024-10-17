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
      """User[\s\t]+<({user}[\w\.\-\!\#\^\~]{1,40}\$?)-({src_host}[\w]+-iPhone)>[\s\t]+IP[\s\t]+<({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?>[\s\t]+(?:IPv4[\s\t])?Address[\s\t]+<({src_translated_ip}[^>]+)>"""
    ]
        ParserVersion = "v1.0.0"
  

}
```