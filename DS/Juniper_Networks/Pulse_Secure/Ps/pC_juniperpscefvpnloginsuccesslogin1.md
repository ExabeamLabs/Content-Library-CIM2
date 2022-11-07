#### Parser Content
```Java
{
Name = juniper-ps-cef-vpn-login-success-login-1
    ParserVersion = v1.0.0
    Vendor = Juniper Networks
    Product = Pulse Secure
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [
"""Agent login succeeded for"""
"""user="""
]
    Fields = [
      """({event_code}Agent login succeeded) for ({user}[^",@\/]+)(?:(@|\/)({domain}[^\/\s]+))?[^=]*? from ({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
      """\(({realm}[^\)]+)\)\[ ]""",
      """({os}iOS|Android|BlackBerry|iPhone OS|Windows Phone|BeOS|(?:W|w)indows\s+\d{1,2}|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)"""
  ]
 

}
```