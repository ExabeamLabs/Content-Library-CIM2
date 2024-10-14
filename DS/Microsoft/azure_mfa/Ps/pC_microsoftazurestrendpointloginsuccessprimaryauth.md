#### Parser Content
```Java
{
Name = "microsoft-azure-str-endpoint-login-success-primaryauth"
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Azure MFA"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""pfsvc: Primary auth succeeded for """
]
Fields = [
"""({host}[\w\.-]+)\s+pfsvc:"""
"""\suser\s+'({user_dn}[^']+)' \(distinguishedName format\)"""
"""\suser\s+'*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^'\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'"""
"""({auth_method}Primary auth)"""
]


}
```