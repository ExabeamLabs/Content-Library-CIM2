#### Parser Content
```Java
{
Name = "microsoft-azuremfa-str-endpoint-login-fail-auth"
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Azure MFA"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""pfsvc: Failed """
""" auth for """
]
Fields = [
"""({host}[\w\.-]+)\s+pfsvc:"""
"""Failed\s+({auth_method}.+?)\s+auth for """
"""\suser\s+'({user_dn}[^']+)' \(distinguishedName format\)"""
"""\suser\s+'({user}[^']+)'"""
"""Logon failure:\s*({failure_reason}.+?)(\s*\(|$)"""
]


}
```