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
      """Username = ({user}[\w\.\-]{1,40}\$?).+?IP = ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\sClient Type:\s+({client_system}.+?)\s+Client Application Version:\s+({client_system_version}[^"]+?)\s*($|\w+=|"|')"""
     ]
  

}
```