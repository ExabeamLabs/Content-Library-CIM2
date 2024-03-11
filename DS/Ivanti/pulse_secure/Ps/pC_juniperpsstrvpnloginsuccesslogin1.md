#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-success-login-1
   ParserVersion = v1.0.0
   Vendor = Ivanti
   Product = Pulse Secure
   TimeFormat = "yyyy-MM-dd HH:mm:ss"
   Conditions = [ 
"""Agent login succeeded for"""
]
  Fields = [
    """({event_name}Agent login succeeded) for (({domain}[^\\]+)[\\])?({user}[^",@\/]+)(?:(@|\\)({=domain}[^\/\s]+))?[^=]*? from ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\(({realm}[^\)]+)\)\[ ]""",
    """({user}[^\s\\]+)\(({realm}[^\)]+)?"""
    """({os}iOS|Android|BlackBerry|iPhone OS|Windows Phone|BeOS|(?:W|w)indows\s+\d{1,2}|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin)"""
    """\[\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\].+?\[({resource}[^\]]+)\]"""
  ]


}
```