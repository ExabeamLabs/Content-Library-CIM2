#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-success-751025
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Adaptive Security Appliance
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """assigned to session""", """-751025""" ]
    Fields = [
      """({time}\d+-\d+-\d+T\d+:\d+:\d+)""",
      """\-\d\d:\d\d\s+({host}[\w.\-]+) : %ASA""",
      """Username:({user}.+?) IKEv2 """,
      """Local:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """Remote:({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """IPv4 Address=(?:0\.0\.0\.0|({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))""",
      """IPv6 address=(?:0\.0\.0\.0|({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))""",
      """Group:({realm}[^\s]+)""",
      """%ASA-({priority}\d+)-({event_code}\d+)"""
    ]
    DupFields = [ "user->account" ]
  

}
```