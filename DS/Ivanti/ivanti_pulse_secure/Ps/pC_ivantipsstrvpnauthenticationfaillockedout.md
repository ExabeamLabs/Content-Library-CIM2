#### Parser Content
```Java
{
Name = ivanti-ps-str-vpn-authentication-fail-lockedout
  ParserVersion = v1.0.0
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssz"
  Conditions = [ """PulseSecure: """, """Authentication requests from IP address """, """ temporarily locked out""" ]
  Fields = [
    """\w{3}\s\d+\s\d+:\d+:\d+\s({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """({time}\d+\-\d+\-\d+T\d+:\d+:\d+-\d+:\d+)\s*({host}[\w\-.]+)\s*PulseSecure:""",
    """\d+\-\d+\-\d+\s\d+:\d+:\d+\s-\s({vpn_client}[^\s]+)\s*\-\s*\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s*[^:]+::({account}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  ]


}
```