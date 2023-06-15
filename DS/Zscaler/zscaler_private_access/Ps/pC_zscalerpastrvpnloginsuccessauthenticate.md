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
    """([^,]*,){2}({email_address}[^\s,]+),([^,]*,){6}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,([^,]*,){3}({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ),[^,]*,({bytes_in}\d+),({bytes_out}\d+)"""
  ]


}
```