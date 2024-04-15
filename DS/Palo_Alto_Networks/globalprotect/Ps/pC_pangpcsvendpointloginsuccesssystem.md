#### Parser Content
```Java
{
Name = "pan-gp-csv-endpoint-login-success-system"
ParserVersion = "v1.0.0"
Vendor = "Palo Alto Networks"
Product = "GlobalProtect"
TimeFormat = "yyyy/MM/dd HH:mm:ss"
Conditions = [
""",SYSTEM,auth,"""
"""AUTH_PROFILE_AZURE"""
""",saml-signature-validated,"""
]
Fields = [
"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+),"""
"""(c|C)lient '({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""for user\s*'({email_address}[^']+)"""
]


}
```