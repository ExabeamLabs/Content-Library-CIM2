#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-logout-success-timeout
    ParserVersion = v1.0.0
    Vendor = Ivanti
    Product = Ivanti Pulse Secure
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [
"""Session timed out for"""
""" (session:"""
]
    Fields = [
      """({time}\d+-\d+-\d+ \d\d:\d\d:\d\d)""",
      """\d{4}-\d{2}-\d{2} \d\d:\d\d:\d\d\s+-\s+({dest_host}({host}[\w\.-]+))\s+-\s+\[""",
      """\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+""",
      """Session timed out for (?:({email_address}[^@\\\/]+@[^@\/\s]+)|(uid[^\/]+\/)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
      """\d\d:\d\d\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s*""",
      """PulseSecure:[\s\-]*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({dest_host}({host}[\w\-.]+))""",
      """PulseSecure:.*?\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+(({domain}[^\\]+)\\+)?(?:({email_address}[^@\\\/]+@[^@\(\s]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\(({realm}[^\)]+)?"""
    ]
  

}
```