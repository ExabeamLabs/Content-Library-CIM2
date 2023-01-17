#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-logout-success-sessiontimedout
  Vendor = Juniper Networks
  Product = Juniper Pulse Secure
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ PulseSecure: """, """session timeout for""", """ (session:""" ]
  Fields = [
    """\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s\d"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s({host}[\w\-.]+)\sPulseSecure:""",
    """\- \[({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\]\s+(({email_address}[^@\s]+@[^.\s]+\.[^\s]+)|({full_name}[^,\[]+,[^\[]+)|(({domain}[^\\\(]+)\\)?(System|({user}[^\(]+)))\(({realm}[^\)]+)?\)\[({resource}[^\]]+)?\]""",
    """session timeout for (({email_address}[^@\s\/]+@[^.\s\/]+\.[^\s\/]+)|({full_name}[^,\/]+,[^\/]+)|(({domain}[^\\\/]+)\\)?|({user}[^\/\s]+))\/""",
    """\s\(({additional_info}session:[^\)]+)\)"""
  ]
  ParserVersion = "v1.0.0"


}
```