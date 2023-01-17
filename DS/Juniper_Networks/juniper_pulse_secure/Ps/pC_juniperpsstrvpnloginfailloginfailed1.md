#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-fail-loginfailed-1
  Vendor = Juniper Networks
  Product = Juniper Pulse Secure
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ PulseSecure: """, """Login failed.""", """Reason:""" ]
  Fields = [
    """\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s\d"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s({host}[\w\-.]+)\sPulseSecure:""",
    """\- \[({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\]\s+(({email_address}[^@\s]+@[^.\s]+\.[^\s]+)|({full_name}[^,\[]+,[^\[]+)|(({domain}[^\\\(]+)\\)?(System|({user}[^\(]+)))\(""",
    """Reason:\s+({failure_reason}[^"]+)"""",
    """({event_name}Login failed)"""
  ]
  ParserVersion = v1.0.0


}
```