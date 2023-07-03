#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-logout-success-sessiontimedout
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ PulseSecure: """, """session timeout for""", """ (session:""" ]
  Fields = [
    """\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s\d"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s({host}[\w\-.]+)\sPulseSecure:""",
    """\- \[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+([\w\s]+?::)?(({email_address}[^@\s]+@[^.\s]+\.[^\s]+)|({full_name}[^,\[]+,[^\[]+)|(({domain}[^\\\(]+)\\)?(System|({user}[^\(]+)))\(({realm}[^\)]+)?\)\[({resource}[^\]]+)?\]""",
    """session timeout for (({email_address}[^@\s\/]+@[^.\s\/]+\.[^\s\/]+)|({full_name}[^,\/]+,[^\/]+)|(({domain}[^\\\/]+)\\)?|({user}[^\/\s]+))\/""",
    """\s\(({additional_info}session:[^\)]+)\)"""
  ]
  ParserVersion = "v1.0.0"


}
```