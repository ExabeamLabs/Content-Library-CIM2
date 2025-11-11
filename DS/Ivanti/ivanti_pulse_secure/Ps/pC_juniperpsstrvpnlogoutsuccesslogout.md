#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-logout-success-logout
    ParserVersion = v1.0.0
    Vendor = Ivanti
    Product = Ivanti Pulse Secure
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [
""" Logout from """
""" (session:"""
]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d) \- .*?Logout from""",
      """(Juniper|PulseSecure):\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({dest_host}({host}[\w\-.]+))""",
      """\d\d:\d\d:\d\d\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s*""",
      """\[\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\]\s+(?:({email_address}[^@\s]+@[^@\s\(]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
      """PulseSecure:.*?\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+(({domain}[^\\]+)\\+)?(?:({email_address}[^@\s]+@[^@\(]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\(({realm}[^\)]+)?""",
      """Logout from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    ]
  

}
```