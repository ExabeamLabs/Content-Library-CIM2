#### Parser Content
```Java
{
Name = "juniper-ps-str-user-delete-fail-firewall"
Vendor = "Ivanti"
Product = "Ivanti Pulse Secure"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""PulseSecure:"""
"""User Accounts modified."""
"""id=firewall"""
]
Fields = [
"""time=\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""vpn=({host}[^\s]+)"""
"""\suser=(\\+)?(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
"""realm=*"({realm}[^\"]+)?\\*"""
"""roles="({role}[^\"]+)?\\*"""
"""Removed username ((({dest_domain}[^\\]+)\\)?(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({account_name}({dest_user}[^\\\s]+))))"""
]
ParserVersion = "v1.0.0"


}
```