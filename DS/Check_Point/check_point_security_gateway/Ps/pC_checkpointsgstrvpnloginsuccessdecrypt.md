#### Parser Content
```Java
{
Name = "checkpoint-sg-str-vpn-login-success-decrypt"
Vendor = "Check Point"
Product = "Check Point Security Gateway"
TimeFormat = "ddMMMyyyy  HH:mm:ss"
Conditions = [
"""%CHKPNT-6-031085: decrypt"""
]
Fields = [
"""decrypt,([^,]*,){33}({time}[^,]+)"""
"""decrypt,([^,]*?,){3}({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""decrypt,([^,]*?,){40}({user}[^,]+)"""
]
ParserVersion = "v1.0.0"


}
```