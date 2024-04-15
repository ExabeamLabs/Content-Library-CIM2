#### Parser Content
```Java
{
Name = "pan-aperture-csv-app-login-success-signin"
Vendor = "Palo Alto Networks"
Product = "Palo Alto Aperture"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""" Aperture """
""",admin_audit,"""
"""sign_in"""
]
Fields = [
"""({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)\s({host}[^\s]+)"""
"""admin_audit,"*({email_address}[^@]+[^,"]+)"*,"""
"""admin_audit,"*([^,]*,){2}({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"*,"""
"""admin_audit,"*([^,]*,){7}"*({action}[^,"]+)"*,"""
]
ParserVersion = "v1.0.0"


}
```