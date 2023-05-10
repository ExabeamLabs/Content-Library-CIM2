#### Parser Content
```Java
{
Name = zscaler-pa-str-vpn-login-success-authenticate
  ParserVersion = v1.0.0
  Vendor = Zscaler
  Product = Zscaler Private Access
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
""",ZPN_STATUS_AUTHENTICATED,"""
  ]
  Fields = [
    """([^,]*,){2}({email_address}[^\s,]+),([^,]*,){6}({src_ip}[A-Fa-f:\d.]+),([^,]*,){3}({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ),[^,]*,({bytes_in}\d+),({bytes_out}\d+)"""
  ]


}
```