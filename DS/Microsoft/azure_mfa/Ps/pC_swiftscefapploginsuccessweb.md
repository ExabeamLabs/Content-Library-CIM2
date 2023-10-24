#### Parser Content
```Java
{
Name = "swift-s-cef-app-login-success-web"
Conditions = [
"""|SWIFT|Alliance Web Platform|"""
"""|login.success|"""
]
ParserVersion = "v1.0.0"

azure-mfa-auth = {
Vendor = "Microsoft"
Product = "Azure MFA"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z\|"""
"""Pfauth (?:failed|succeeded) for user '(?:({email_address}[^@']+@[^']+)|({user}[\w\.\-]{1,40}\$?))'"""
"""Call status:\s*({call_status}.+?)\s*-\s*\""""
"""Pfauth failed for user.*?\-\s*\"({failure_reason}[^\"]+)\""""
"""({auth_method}Pfauth)"""
"""\sfrom\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(:({src_port}\d+))?"""

}
```