#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-success-connected
  ParserVersion = v1.0.0
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
"""PulseSecure: """
""" Connected to """
""" ["""
]
  Fields = [
    """PulseSecure:.+?({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({host}[\w\-.]+)""",
    """\s+-\s+\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]""",   
    """\s+-\s+\[[^\]]+\]\s+([\w\s]+?::)?(({email_address}[^@\s\(]+@[^\.\s\(]+\.[^\s]+)|(({domain}[^\(]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))\(({realm}[^\)]+)?\)""",
    """\sConnected to\s+(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\.-]+))\s+port"""
  ]
  DupFields = [ "user->account" ]


}
```