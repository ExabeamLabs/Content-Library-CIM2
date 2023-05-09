#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-success-passed
    ParserVersion = v1.0.0
    Vendor = Ivanti
    Product = Ivanti Pulse Secure
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Conditions = [ 
"""Host Checker policy """
""" passed on host """
"""PulseSecure:"""
]
    Fields = [
      """passed on host '({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""", """({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+PulseSecure:((\s\S+){3}\s|\s+)({time}\d\d\d\d\-\d\d-\d\d \d\d:\d\d:\d\d)\s+(\S+\s+){3}\[\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\]\s+({user}[^\s\(\)]+)\((|unknown|({realm}[^)]+))\)""",
      """for user '({user}[^']+)'""",
      """({host}[\w.\-]+) PulseSecure:"""
    ]
    DupFields = [ "dest_ip->host" , "user->account" ]
  

}
```