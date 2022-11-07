#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-success-713184
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Adaptive Security Appliance
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Conditions = [ """-713184""", """%ASA-""" ]
    Fields = [
      """({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
      """%ASA-({priority}\d)-({event_code}\d+)""",
      """Username = ({user}[^,@]+).+?IP = ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """\sClient Type:\s+({client_system}.+?)\s+Client Application Version:\s+({client_system_version}[^"]+)"""
     ]
  

}
```