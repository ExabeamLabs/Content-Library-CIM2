#### Parser Content
```Java
{
Name = juniper-ps-cef-vpn-login-fail-loginfailed
    ParserVersion = v1.0.0
    Vendor = Juniper Networks
    Product = Pulse Secure
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ 
"""Login failed using auth server"""
"""Reason:"""
"""vpn="""
"""user="""
]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """\stime="({time}[^"]+)"""",
      """\w+\s*\d+\s*\d\d:\d\d:\d\d\s*({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-\.]+)))\s*:\s*\(""",
      """\svpn=({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-\.]+)))\s""",
      """\s+({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+)))\s+PulseSecure:""",
      """\d\d:\d\d:\d\d\s+-\s+\[({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\]\s+(({domain}[^\\]+)\\)?(?:({email_address}[^@]+@[^@(]+)|({user}.+?))\(""",
      """Reason:\s+({failure_reason}[^"]+?)\s*("|$)""",
      """src=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """user=(({domain}[^\\]+)\\)?(?:({email_address}[^@\s]+@[^@\s]+)|({user}.+?))\s+\w+=""",
      """msg="[^\:]+:\s*({failure_reason}[^\-\.]+)\.\s*"""
    ]
  

}
```