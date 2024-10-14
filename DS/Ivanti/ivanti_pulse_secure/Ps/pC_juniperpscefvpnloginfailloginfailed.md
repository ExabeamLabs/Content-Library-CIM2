#### Parser Content
```Java
{
Name = juniper-ps-cef-vpn-login-fail-loginfailed
    ParserVersion = v1.0.0
    Vendor = Ivanti
    Product = Ivanti Pulse Secure
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
      """\w+\s*\d+\s*\d\d:\d\d:\d\d\s*(::ffff:)?({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-\.]+)))""",
      """\svpn=({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-\.]+)))\s""",
      """\s+({host}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+)))\s+PulseSecure:""",
      """\d\d:\d\d:\d\d\s+-\s+\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+(({domain}[^\\]+)\\)?(?:({email_address}[^@]+@[^@(]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\(""",
      """msg="[^\:]+:\s*({failure_reason}[^\-\.]+)\.\s*""",
      """Reason:\s+({failure_reason}[^"]+?)\s*(\s|"|$)""",
      """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\suser=(\\+)?(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({user}[\w\.\-]+))(\s+\w+=|\s*$)""",
    ]
  

}
```