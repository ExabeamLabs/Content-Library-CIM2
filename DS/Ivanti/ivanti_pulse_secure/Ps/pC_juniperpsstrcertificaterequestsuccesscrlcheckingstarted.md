#### Parser Content
```Java
{
Name = juniper-ps-str-certificate-request-success-crlcheckingstarted
  Vendor = Ivanti
  Product = Ivanti Pulse Secure
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssz"]
  Conditions = [ """ PulseSecure: """, """CRL checking started for certificate""" ]
  Fields = [
    """\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+({dest_host}({host}[\w\-.]+))\s\d"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d([+-]\d\d:\d\d)?)\s+({dest_host}({host}[\w\-.]+))\s+PulseSecure:""",
    """\- \[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\s+(({email_address}[^@\s]+@[^.\s]+\.[^\s]+)|({full_name}[^,\[]+,[^\[]+)|(({domain}[^\\\(]+)\\)?(System|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\(({realm}[^\)]+)?\)\[({resource}[^\]]+)?\]\s(\-\s)?({additional_info}.+?)$""",
    """({event_name}CRL checking started for certificate)""",
    """emailAddress=({email_address}[^@,\s]+?@[^@,\s.]+\.[^@,\s]+)""",
    """ CN="+({full_name}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```