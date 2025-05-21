#### Parser Content
```Java
{
Name = "microsoft-azuremfa-str-endpoint-login-success-callstatus-1"
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Azure MFA"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""pfsvc: Pfauth succeeded """
"""Call status:"""
]
Fields = [
"""({host}[\w\.-]+)\s+pfsvc:"""
"""\suser\s+'({user_dn}[^']+)' \(distinguishedName format\)( from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)?\.\s"""
"""\suser\s+'(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^'\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))'\s*( from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)?\.\s"""
"""\WCall status:\s*({call_status}\S+)\s+-\s*\"({failure_reason}[^\"]+)\"\."""
"""({auth_method}Pfauth)"""
]


}
```