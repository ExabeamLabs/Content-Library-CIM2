#### Parser Content
```Java
{
Name = juniper-ps-str-network-notification-success-transportmodeswitched
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ PulseSecure: """, """Transport mode switched over to SSL""" ]
  Fields = [
    """\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s\d"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s({host}[\w\-.]+)\sPulseSecure:""",
    """\- \[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+([\w\s]+?::)?(({email_address}[^@\s]+@[^.\s]+\.[^\s]+)|({full_name}[^,\[]+,[^\[]+)|(({domain}[^\\\(]+)\\)?(System|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\(({realm}[^\)]+)?\)\[({resource}[^\]]+)?\]""",
    """({additional_info}({event_name}Transport mode switched over to SSL for user) with NCIP ({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))"""
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```