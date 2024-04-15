#### Parser Content
```Java
{
Name = "checkpoint-sg-str-vpn-login-success-authcrypt"
Vendor = "Check Point"
Product = "Check Point Security Gateway"
TimeFormat = "ddMMMyyyy HH:mm:ss"
Conditions = [
"""%CHKPNT-6-031085: authcrypt"""
"""connected to gateway"""
]
Fields = [
"""connected to gateway,([^,]*,){14}({time}[^,]+)"""
"""authcrypt,([^,]*?,){3}({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""connected to gateway,([^,]*?,)({user}[^,]+)"""
]
ParserVersion = "v1.0.0"


}
```