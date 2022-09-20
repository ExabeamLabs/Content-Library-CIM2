#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-success-succeeded
    ParserVersion = v1.0.0
    Vendor = Juniper Networks
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
      """PulseSecure:.*?\[(::ffff:)?({src_ip}[a-fA-F:\d.]+)\]\s+(({domain}[^\\]+)\\)?(?:({email_address}[^@\s]+@[^@\(]+)|({user}[^\s]+))\(({realm}[^\)]+)?""",
      """Login succeeded for (?:({email_address}[^@\s]+@[^@\s\/]+)|({user}[^\s\/]+))""",
      """Login succeeded for [^/]+/({realm}.+?)\s+\(session:""",
      """Login succeeded for .+?from (::ffff:)?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """PulseSecure:.*?\[(::ffff:)?({src_ip}[a-fA-F:\d.]+)\]\s+(({domain}[^\\]+)\\)?(?:({email_address}[^@\s]+@[^@\(]+)|({user}[^\s\\]+))\(({realm}[^\)]+)?""",
    ]
    DupFields = [ "host->dest_host" , "user->account" ]
  

}
```