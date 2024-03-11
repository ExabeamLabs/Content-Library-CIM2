#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-success-succeeded
    ParserVersion = v1.0.0
    Vendor = Ivanti
    Product = Pulse Secure
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Conditions = [
""" Login succeeded for """
""" (session:"""
]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d) \- .*?Login succeeded for""",
      """PulseSecure:\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({host}[\w\-.]+)""",
      """(::ffff:)?({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|[\w\-\.]+)\s*(Juniper|PulseSecure):""",
      """PulseSecure:.*?\[(::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+(({domain}[^\\]+)\\)?(?:({email_address}[^@\s]+@[^@\(]+)|({user}[^\s]+))\(({realm}[^\)]+)?""",
      """Login succeeded for (?:({email_address}[^@\s]+@[^@\s\/]+)|({user}[^\s\/]+))""",
      """Login succeeded for [^/]+/({realm}.+?)\s+\(session:""",
      """Login succeeded for .+?from (::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """PulseSecure:.*?\[(::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+(({domain}[^\\]+)\\)?(?:({email_address}[^@\s]+@[^@\(]+)|({user}[^\s\\]+))\(({realm}[^\)]+)?""",
    ]
    DupFields = [ "host->dest_host" , "user->account" ]
  

}
```