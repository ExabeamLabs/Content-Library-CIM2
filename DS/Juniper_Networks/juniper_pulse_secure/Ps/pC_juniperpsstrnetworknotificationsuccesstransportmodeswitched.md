#### Parser Content
```Java
{
Name = juniper-ps-str-network-notification-success-transportmodeswitched
  Vendor = Juniper Networks
  Product = Juniper Pulse Secure
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ PulseSecure: """, """Transport mode switched over to SSL""" ]
  Fields = [
    """\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s\d"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s({host}[\w\-.]+)\sPulseSecure:""",
    """\- \[({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\]\s+(({email_address}[^@\s]+@[^.\s]+\.[^\s]+)|({full_name}[^,\[]+,[^\[]+)|(({domain}[^\\\(]+)\\)?(System|({user}[^\(]+)))\(({realm}[^\)]+)?\)\[({resource}[^\]]+)?\]""",
    """({additional_info}({event_name}Transport mode switched over to SSL for user) with NCIP ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))"""
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```