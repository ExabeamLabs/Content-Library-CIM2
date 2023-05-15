#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-logout-success-loggedout
  ParserVersion = v1.0.0
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
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
    """\suser started new session from IP \(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\)"""
  ]
  DupFields = [ "dest_host->host" ]


}
```