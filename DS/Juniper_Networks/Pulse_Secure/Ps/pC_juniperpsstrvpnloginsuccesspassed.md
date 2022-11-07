#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-success-passed
    ParserVersion = v1.0.0
    Vendor = Juniper Networks
    Product = Pulse Secure
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Conditions = [ 
"""Host Checker policy """
""" passed on host """
"""PulseSecure:"""
]
    Fields = [
      """passed on host '({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""", """({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+PulseSecure:((\s\S+){3}\s|\s+)({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)\s+(\S+\s+){3}\[\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\]\s+({user}[^\s\(\)]+)\((|unknown|({realm}[^)]+))\)""",
      """for user '({user}[^']+)'""",
      """({host}[\w.\-]+) PulseSecure:"""
    ]
    DupFields = [ "dest_ip->host" , "user->account" ]
  

}
```