#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-logout-success-ended
  ParserVersion = v1.0.0
  Vendor = Juniper Networks
  Product = Juniper Pulse Secure
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
""": Session ended for user"""
]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",    
    """({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+)))\s*:\s*\S+\s*\-\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d).*?: Session ended for user""",
    """PulseSecure:\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)\s+\-\s+({host}[\w\-.]+)""",
    """\s+({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w-.]+)))\s+PulseSecure:""",
    """with IP(?:v4 address)?\s+({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """PulseSecure:\s*\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+\-\s+(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+))""",
    """\s(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))\s+(Juniper|PulseSecure):""",
    """\- \[({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\]"""
    """\- \[({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\]\s+(\w+\\)?([\w\s]+?::)?(({email_address}[^@\s]+@[^(@]+)|(({domain}[^\\\(]+)\\+)?({user}[^\(]+))\([^\[]+\)\[(?!Machine Cert)"""
 ]


}
```