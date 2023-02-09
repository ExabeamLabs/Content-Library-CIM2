#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-logout-success-timeout
    ParserVersion = v1.0.0
    Vendor = Juniper Networks
    Product = Juniper Pulse Secure
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [
"""Session timed out for"""
""" (session:"""
]
    Fields = [
      """({time}\d+-\d+-\d+ \d\d:\d\d:\d\d) \-""",
      """\d{4}-\d{2}-\d{2} \d\d:\d\d:\d\d\s+-\s+({host}[\w\.-]+)\s+-\s+\[""",
      """\[({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\]\s+""",
      """Session timed out for (?:({email_address}[^@\\\/]+@[^@\/\s]+)|({user}[^/]+))""",
      """\d\d:\d\d\s*({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*""",
      """PulseSecure:[\s\-]*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({host}[\w\-.]+)""",
      """PulseSecure:.*?\[({src_ip}[a-fA-F:\d.]+)\]\s+(({domain}[^\\]+)\\)?(?:({email_address}[^@\\\/]+@[^@\(\s]+?)|({user}[^\s]+))\(({realm}[^\)]+)?"""
    ]
    DupFields = [ "host->dest_host" ]
  

}
```