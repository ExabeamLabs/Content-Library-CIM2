#### Parser Content
```Java
{
Name = pan-aperture-csv-app-logout-success-signout
  Vendor = Palo Alto Networks
  Product = Palo Alto Aperture
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ Aperture """, """,admin_audit,""","""sign_out""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)\s({host}[^\s]+)""",
    """admin_audit,"*({email_address}[^@]+[^,"]+)"*,"""
    """admin_audit,"*([^,]*,){2}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"*,""",
    """admin_audit,"*([^,]*,){7}"*({action}[^,"]+)"*,"""
  ]


}
```