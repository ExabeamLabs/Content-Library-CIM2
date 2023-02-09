#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-logout-success-loggedout
  ParserVersion = v1.0.0
  Vendor = Juniper Networks
  Product = Juniper Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
""" PulseSecure:"""
""" logged out from """
""" because user started new session """
]
  Fields = [
    """({time}\d\d\d\d\-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\s({dest_host}[^\s]+)\s+PulseSecure:""",
    """\]\s\-\s+?(({email_address}[^@]+@[^\s<]+?)|({user}[^\s]+))\/\S+\s+logged out from""",
    """\suser started new session from IP \(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\)"""
  ]
  DupFields = [ "dest_host->host" ]


}
```