#### Parser Content
```Java
{
Name = juniper-ps-cef-vpn-login-fail-loginfailed
    ParserVersion = v1.0.0
    Vendor = Juniper Networks
    Product = Juniper Pulse Secure
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
      """\w+\s*\d+\s*\d\d:\d\d:\d\d\s*(::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-\.]+)))""",
      """\svpn=({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-\.]+)))\s""",
      """\s+({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+)))\s+PulseSecure:""",
      """\d\d:\d\d:\d\d\s+-\s+\[({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\]\s+(({domain}[^\\]+)\\)?(?:({email_address}[^@]+@[^@(]+)|({user}.+?))\(""",
      """msg="[^\:]+:\s*({failure_reason}[^\-\.]+)\.\s*""",
      """Reason:\s+({failure_reason}[^"]+?)\s*(\s|"|$)""",
      """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """user=(({domain}[^\\]+)\\)?(?:({email_address}[^@\s]+@[^@\s]+)|({user}.+?))\s+\w+=""",
    ]
  

}
```