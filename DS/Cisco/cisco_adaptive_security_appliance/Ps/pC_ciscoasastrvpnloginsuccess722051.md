#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-success-722051
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Adaptive Security Appliance
    TimeFormat = ["MMM dd yyyy HH:mm:ss","yyyy-MM-dd'T'HH:mm:ssZ"]
    Conditions = [ """assigned to session""", """-722051""" ]
    Fields = [
      """Group <({realm}[^<>\s]+?)>""",
      """({time}\w+ \d+ (\d\d\d\d )?\d+:\d+:\d+)""",
      """[\s\t]+\d\d:\d\d:\d\d\s+({host}[\w.\-]+) : %ASA""",
      """({host}[^\s]+)\s+:\s+%FTD-""",
      """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
      """User[\s\t]+<(({domain}[^\\\/]+)[\\\/])?(?![^\s]+@[^\s]+)({user}[\w\.\-]{1,40}\$?)>[\s\t]+IP[\s\t]+<({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?>[\s\t]+(?:IPv4[\s\t])?Address[\s\t]+<({src_translated_ip}[^>]+)>"""
      """User[\s\t]+<({email_address}[^>@]+@[^>@]+)>[\s\t]+IP[\s\t]+<({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?>[\s\t]+(?:IPv4[\s\t])?Address[\s\t]+<({src_translated_ip}[^>]+)>""",
      """%ASA-({priority}\d+)-({event_code}\d+)""",
      """%FTD-({priority}\d+)-({event_code}\d+)""",
      """\sGroup\s*<({group_name}[^>]+)>"""
      """\sUser\s*<({user}[\w\.\-]{1,40}\$?)>"""
    ]
  

}
```