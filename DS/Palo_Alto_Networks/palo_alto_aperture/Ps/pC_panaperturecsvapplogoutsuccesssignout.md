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
    """admin_audit,"*([^,]*,){2}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"*,""",
    """admin_audit,"*([^,]*,){7}"*({action}[^,"]+)"*,""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]


}
```