#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-success-started
    ParserVersion = v1.0.0
    Vendor = Juniper Networks
    Product = Pulse Secure
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ 
"""PulseSecure:"""
""": Session started for user"""
"""Network"""
]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\s-\s""",
      """({host}[\w\-\.]+)\s*:\s*\S+\s*\-\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d).*?: Session started for user""",
      """({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|[\w\-\.]+)\s*(Juniper|PulseSecure):""",
      """PulseSecure:\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({host}[\w\-.]+)""",
      """\s+({host}[\w-.]+)\s+PulseSecure:""",
      """PulseSecure:\s*\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+\-\s+({dest_host}[\w\-.]+)""",
      """,\s+hostname\s+({src_host}[\w.\-]+)""",
      """\s(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))\s+(Juniper|PulseSecure):""",
      """\- \[({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\]"""
      """\- \[({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\]\s+([\w\s]+?::)?(({domain}[^\\]+)\\)?({user}[^\(]+)\(({realm}[^\[]+)?\)\[(?!Machine Cert)"""
    ]
    DupFields = [ "host->dest_host" , "user->account" ]
  

}
```