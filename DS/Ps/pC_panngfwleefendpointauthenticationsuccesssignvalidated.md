#### Parser Content
```Java
{
Name = "pan-ngfw-leef-endpoint-authentication-success-signvalidated"
Conditions = [
"""LEEF:"""
"""|Palo Alto Networks|PAN-OS Syslog Integration|"""
"""type=auth"""
"""|saml-signature-validated|"""
]
ParserVersion = "v1.0.0"

leef-paloalto-vpn-event.Fields}[
      """usrName =(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
      
}
```