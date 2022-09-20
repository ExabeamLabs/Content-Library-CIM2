#### Parser Content
```Java
{
Name = juniper-ps-cef-vpn-login-success-connected-2
  ParserVersion = v1.0.0
  Vendor = Juniper Networks
  Product = Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
""": User with IP """
""" connected with """
"""VPN Tunneling:"""
"""dstname="""
]
  Fields = [
    """\stime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\sfw=(::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-\.]+)))""",
    """\s+(::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+)))\s+(Juniper|PulseSecure):""",
    """user=({user}[^\s]+)""",
    """: User with IP ({src_translated_ip}[A-Fa-f\d:.]+)""",
    """src=({src_ip}[A-Fa-f\d:.]+)"""
  ] 
  DupFields = [ "user->account" ] 


}
```